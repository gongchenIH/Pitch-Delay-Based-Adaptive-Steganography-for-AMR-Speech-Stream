# PDAS-Pitch Delay Based Adaptive Steganography for AMR Speech Stream

##  说明

​        现有自适应码本隐写算法会破坏基音延迟的短时稳定性，以基音延迟二阶差分值设计的自适应码本隐写分析特征取得了较好的攻击性能。为了提高自适应码本隐写算法的安全性能，设计了基于最小加性失真代价的框架的自适应隐写算法。我们利用基音延迟的差分值衡量失真代价，利用STC实现了最小加性失真代价并保证了消息的嵌入和提取。

​        Sample文件夹提供了对应的样本文件，其中：

​        Test.wav是载体语音文件，分别用来生成cover和stego语音文件，Test.pcm是去处头文件后的语音文件，AMR编码要求的pcm文件；

​       cover.amr是没有嵌入消息的压缩语音文件，cover.txt是cover.amr解码的基音延迟，cover.pcm是cover.amr解码后的语音文件，cover.wav是cover.pcm加上头文件后的语音文件；

​        stego.amr是采用了相对嵌入率0.5的压缩语音文件，stego.txt是stego.amr解码的基音延迟，stego.pcm是stego.amr解码后的语音文件，stego.wav是stego.pcm加上头文件后的语音文件。

## 语音质量

​        下图显示的嵌入前后，cover.wav和stego.wav的频谱图。可以看到嵌入前后对语音质量的影响较小，人耳几乎感觉不到差别。

![image](https://github.com/gongchenIH/Pic/blob/master/Spectrum_compare.png)

## 嵌入效果

​        下图显示的嵌入前后，提取的cover.amr和stego.amr的基音延迟。可以看到嵌入位置主要分布在基音延迟变化较大的位置，在这些位置嵌入消息可以减少对基音延迟的短时稳定性的影响，从而达到提升算法安全性的目的。

![image](https://github.com/gongchenIH/Pic/blob/master/PD_compare.png)

## 参考论文

#### 1. [隐写算法](https://github.com/gongchenIH/Speech-Steganography-in-Compressed-Domian/tree/main/1-Steganography/1.1.1-PD_Steganpgraphy_Embed_byte)

- **Huang**: Yongfeng Huang, Chenghao Liu, Shanyu Tang and Sen Bai. (2012). [Steganography integration into a low-bit rate speech codec](https://ieeexplore.ieee.org/abstract/document/6301705). *IEEE transactions on information forensics and security*, *7*(6), 1865-1875.


#### 2. [隐写分析算法](https://github.com/gongchenIH/Speech-Steganography-in-Compressed-Domian/tree/main/2-Steganalysis/2.3-PD_Steganalysis)

- **MSDPD**:  Yanzhen Ren, Jing Yang, Jinwei Wang and Lina Wang. [AMR steganalysis based on second-order difference of pitch delay](https://ieeexplore.ieee.org/abstract/document/7774981). *IEEE Transactions on Information Forensics and Security*, *12*(6), 1345-1357.

# PDAS-Pitch Delay Based Adaptive Steganography for AMR Speech Stream

## Abstract

​    Most existing speech steganography breaks the continuity of adjacent pitch delay, which obviously degrades their statistically undetectability. This paper presents a novel steganographic scheme for low bit-rate speech stream against pitch delay steganalysis. Three measures are adopted to enhance steganographic security. First, the short-term stability of pitch delay and the statistical distribution of adjacent sub-frame are considered for designing a distortion function. Second, syndrome-trellis codes (STCs) is utilized to minimize the overall embedding impact based on the defined distortion function. Third, the suboptimal pitch delay is searched to maintain speech quality. Experimental results demonstrate that our scheme achieves higher level of security, especially in the case of low embedding rate. When the relative embedding rate is 0.2 for 10.2 kbit/s AMR stream, the test error rate of our method rises by 12.44% compared with the existing algorithm.

​    The Sample folder provides corresponding sample files, among which:

​     Test.wav is the carrier voice file, which is used to generate cover and stego voice files, respectively, Test.pcm is the voice file after removing the header file, and the pcm file required by AMR encoding;

​     cover.amr is a compressed voice file without embedded messages, cover.txt is the pitch delay decoded by cover.amr, cover.pcm is the voice file decoded by cover.amr, and cover.wav is the cover.pcm plus the header file Voice file

​     stego.amr is a compressed voice file with a relative embedding rate of 0.5, stego.txt is the pitch delay decoded by stego.amr, stego.pcm is the voice file decoded by stego.amr, and stego.wav is stego.pcm plus the header Voice file after the file.

## Voice Quality

​    The following figure shows the spectrogram of cover.wav and stego.wav before and after embedding. It can be seen that the impact on the voice quality before and after embedding is small, and the human ear can hardly feel the difference.

## Embedding Effect

​    The figure below shows the pitch delay of the extracted cover.amr and stego.amr before and after embedding. It can be seen that the embedding positions are mainly distributed in the positions where the pitch delay changes greatly. Embedding messages in these positions can reduce the impact on the short-term stability of the pitch delay, thereby achieving the purpose of improving the security of the algorithm.

## Reference paper

#### 1. [Steganography](https://github.com/gongchenIH/Speech-Steganography-in-Compressed-Domian/tree/main/1-Steganography/1.1.1-PD_Steganpgraphy_Embed_byte)

- **Huang**: Yongfeng Huang, Chenghao Liu, Shanyu Tang and Sen Bai. (2012). [Steganography integration into a low-bit rate speech codec](https://ieeexplore.ieee.org/abstract/document/6301705). *IEEE transactions on information forensics and security*, *7*(6), 1865-1875.


#### 2. [Stgeganalysis](https://github.com/gongchenIH/Speech-Steganography-in-Compressed-Domian/tree/main/2-Steganalysis/2.3-PD_Steganalysis)

- **MSDPD**:  Yanzhen Ren, Jing Yang, Jinwei Wang and Lina Wang. [AMR steganalysis based on second-order difference of pitch delay](https://ieeexplore.ieee.org/abstract/document/7774981). *IEEE Transactions on Information Forensics and Security*, *12*(6), 1345-1357.

