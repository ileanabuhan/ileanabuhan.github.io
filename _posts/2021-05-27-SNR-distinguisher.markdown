---
layout: post
title:  "Using the Signal-to-Noise Ratio (SNR) as a distinguisher"
date:   2021-05-27 11:21:09 +0100
categories: leakage detection
authored: Ileana Buhan
---



In this post, we explore how to use SNR as a distinguisher. To follow along, [download](https://zenodo.org/record/4742593#.YK8drmYzYUo) the trace set and [the notebook.](https://github.com/ileanabuhan/LeakageAssessment/blob/main/SNR-as-distingusher.ipynb) Our goal is to recover the TARGET_BYTE, which for this example is Byte 0 of the S-box out operation, Round 1(of an unprotected software AES implementation). By changing the value of the variable TARGET_BYTE in the provided notebook, you can recover other bytes.  

**Using SNR as a distinguisher**

A *distinguisher* is a scoring function that ranks key candidates. If we measured, processed and chose the correct leakage model, a distinguisher will give the highest score to the valid key candidate.

![SNR_computation]({{site.url}}/assets/img/post_05_27/SNR_computation.png){:class="img-responsive"}

One difference to the [previous example](https://ileanabuhan.github.io/general/2021/05/07/SNR-tutorial.html) is that we have to compute not one SNR trace but 256 traces, one for each possible value of the TARGET_BYTE. The figure above illustrates the computation of the SNR trace for one key candidate (depicted by the small yellow square). As the value of the key candidate changes, the value of the intermediate value changes as well (shown as the small dark blue square). The last step before computing the SNR trace is to group the traces (illustrated by the buckets in the figure) according to the respective value of the TARGET_BYTE (in the previous example, this was green and blue zebras). For our example N, the number of traces is 10000, and each trace has 15000 samples. 

**Does it really work?**

In other words, can we recover the correct key value? There is only one way to find out: run the notebook and see the results.  I have already done it and obtained the figure below, where the traces with the maximum SNR trace correspond to the correct byte. Yay.. \o/ !

![SNR_trace_all]({{site.url}}/assets/img/post_05_27/SNR_all_trace.png){:class="img-responsive"}

**How well does it work?**

This question is more tricky. Remember that identifying the correct key means identifying the SNR trace, which contains the max SNR value (all traces, all samples). One way to determine how well our distinguisher works is to compare the first key candidate with the second key candidate. So let us take a closer look and observe the difference between the peaks of the first and secod value (blue circle in the figure below).

![SNR_trace_all]({{site.url}}/assets/img/post_05_27/SNR_top_2.png){:class="img-responsive"}

 Hmm.. it seems they are pretty close...In fact, when examining the values, we see the maximum SNR value is 0.61 and was obtained for sample 2324. The second-largest value was obtained for sample 2216 and is 0.59. Because we know the correct byte (one of the perks of programming the target and collecting the traces), we know that the SNR distinguisher gave us a valid value.  But if we didn't, the difference is not large enough to inspire confidence in the results.  In some situations it is easy to use the recovered key directly to verify the result, but sometimes this value needs to be used in subsequent attack stages (e.g. when combining the key bytes) and ideally we would want a bit more confidence.

**How does it compare to the correlation distingusher (CPA)?**

This one is for the savvy reader... I did run a CPA attack on the same traces using the same leakage model..

![SNR_trace_all]({{site.url}}/assets/img/post_05_27/Correlation_all.png){:class="img-responsive"}

My conclusion (I know.. one dataset, one experiment..) is that although SNR can work as a distinguisher, I would not replace the CPA distinguisher just yet. If you run the code in the provided notebook on other traces, I would be curious to learn your conclusions. 



