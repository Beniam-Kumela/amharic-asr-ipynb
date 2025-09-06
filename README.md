# amharic-asr-ipynb

This repo implements a [DeepSpeech2](https://arxiv.org/pdf/1512.02595)-like speech recognition model and trains it on an [Amharic dataset](https://github.com/getalp/ALFFA_PUBLIC/tree/master/ASR/AMHARIC). This is meant to host the code discussed in this [video]().

We stress that the main purpose of this model is as a teaching resource as the implementation is more beginner-friendly than the current state-of-the-art (SOTA). Specifically, we find that the final model has a character error rate (CER) of ~23% which is worse than the [SOTA trained on the same dataset](https://huggingface.co/agkphysics/wav2vec2-large-xlsr-53-amharic) which achieved a CER of ~7%. 

The model only takes ~20 epochs (which totals to 2-3 hrs of training time on Google Colab GPUs) to converge as shown by the loss curves.

<img width="846" height="470" alt="image" src="https://github.com/user-attachments/assets/50c79451-93b0-4945-aefe-c86ec76d0381" />


Some predictions from the model are shown below.

```
True : እንደ ገና ኢትዮጵያዊ ለ መሆን መደራደር የ መረጡ ም አሉ
Pred: እንደ ገና ኢትዮጵያዊ ለ መሆን መደራድር የ መረጡ ህሉ
CER: 11.11111111111111 %

True : ስለ ጦርነቱ መናገር በ እነሱ ስለሚ ያምር ጉዳዩ ን ለ እነሱ መተው በ ፈቀድኩ
Pred: ስለ ጥርምነቱ መናገር በ እነሱ ስለሚየመር ጉዳዩ ን ለነሱ መተው በፈቀም
CER: 20.408163265306122 %

True : ለ ዜጐቻቸው የተደላደለ ኑሮ ፈጥረው ከ ተለያዩ ሀገሮች የ መጡ ስደተኞች ን ያስተናግ ዳሉ በ ማለት በልዩ አይ ን እንመለከታ ቸው ይሆናል
Pred: ለ ዜጐቻቸው የተደላደረ ኑሮ ፈጥረው ከ ተለያዩ አገሮች የ መቶ ስደተኞች ን ያስተናግዳሉ በ ማለት መልዩዮ አይን ን መልከታቸው ይሆናል
CER: 12.790697674418606 %
```

Please feel free to open any pull requests if there are any problems with running this code or if there are additional functionalities you would like to see implemented.
