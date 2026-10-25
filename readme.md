# [DRIS]Disruptive Hidden Communication! DRIS technology achieves synchronous detection and passive interference, without channel knowledge or additional power consumption. [Included MATLAB code]

Personal Blog: https://www.cnblogs.com/EWFrontier  
✿Disrupting Covert Communication! DRIS Technology Achieves Synchronous Detection and Passive Interference, Without Channel Knowledge or Extra Power Consumption ✿1. Article Title: Synchronous Detection and Passive Interference Techniques for Covert Communication Based on the Disco Reconfigurable Intelligent Surface (DRIS)
2. Abstract: Covert communication offers stronger privacy protection compared to cryptography and physical layer security (PLS), but existing research in covert communication assumes the channel is reciprocal (i.e., the wireless channel remains constant or nearly constant over the coherence time). This paper investigates the impact of a Disco Reconfigurable Intelligent Surface (DRIS) deployed by monitor Willie on covert communication—the DRIS plays the role of a "Disco Ball" by randomly time-varying reflection coefficients, introducing time-varying full passive interference (FPJ), thereby breaking the assumption of channel reciprocity. The DRIS does not require Bob's channel information nor additional interference power, capable of disrupting Alice and Bob's covert transmission while reducing Willie's detection error rate. To quantify the impact of the DRIS on covert communication, this paper first designs a detection rule for Willie considering the time-varying FPJ with the DRIS, defining false alarm rate (FAR), missed detection rate (MDR) as Willie's detection performance indicators, and signal-to-interference-plus-noise ratio (SJNR) as the communication performance indicator for Alice-Bob covert transmission. Based on this detection rule, we derive the detection threshold for Willie to determine whether communication occurs, and conduct theoretical analysis on Willie's FAR, MDR, and Bob's SJNR, revealing the unique properties of DRIS-based FPJ in covert communication. Finally, numerical simulations validate the effectiveness of the theoretical analysis and assess the impact of the DRIS on covert communication.
3. Introduction
Due to the broadcast and superposition characteristics of wireless channels, wireless systems are inherently vulnerable to various malicious attacks. This issue is particularly critical in the Internet of Things (IoT) era—data transmitted in IoT often contains sensitive personal information such as health and location, and in government and military scenarios, communication concealment is even more crucial. Therefore, research on transmission security and privacy protection has rapidly developed. Covert communication (also known as low detection probability communication) hides the transmission signal within environmental noise to avoid detection by adversarial monitors, with a privacy protection level superior to cryptography and physical layer security (PLS)—if the monitor Willie does not detect the transmission, he will not attempt to decode the information in the signal.
Early studies have established the basic limits of covert communication: in an additive Gaussian white noise (AWGN) channel between Alice and Willie, it is possible to transmit o(√n) bits in n transmissions without knowing the noise power, and the detection probability can be arbitrary low; if the lower bound of noise power is known, then O(√n) bits can be transmitted. Subsequent studies have further improved covert communication performance through non-orthogonal multiple access (NOMA), Turbo coding, relay cooperation, and artificial noise technologies, all assuming the immutability of time-division duplexing (TDD) channels.
Reconfigurable intelligent surfaces (RIS) as a key technology for improving wireless communication performance, adjust the reflection coefficients through a large number of programmable reflective units to enhance system performance without significantly increasing power consumption and cost, and their application in covert communication has been preliminarily explored. However, the emergence of Disco RIS has broken the assumption of channel immutability—the reflection coefficients of Disco RIS are random and time-varying, which can introduce active channel aging (ACA), even destroying the immutability of TDD channels during the coherent time of the channel, and without the knowledge of legitimate user channel information or additional interference power, full-passive jamming (FPJ) can be initiated.
This paper proposes an innovative approach to exploiting the interchangeability of channels in covert communication through the use of DRIS. The main contributions include: constructing a covert communication model under the presence of DRIS, designing Willie's detection rules and performance metrics; deriving statistical characteristics of channels under DRIS impact, detection thresholds, and closed expressions for FAR and MDR, analyzing the asymptotic properties of SJNR; revealing the unique properties of DRIS-based FPJ; and verifying the accuracy of theoretical analysis through simulation.
IV. Method Introduction 1. System Model Design✧
Scenario Deployment: Alice conducts a covert transmission to Bob, with Willie deploying an N_D unit DRIS (controlled by an FPGA controller) that is positioned close to Alice. Willie and Bob are located in the far-field region of the DRIS. The reflection coefficients of the DRIS (phase and amplitude) vary randomly over time and independently follow a distribution, supporting b-bit quantization.
✧  
Channel Models: Direct Channels (Alice-Bob, Alice-Willie) and DRIS-related Channels (DRIS-Bob, DRIS-Willie) use the far-field Gaussian model; Alice-DRIS channel employs the near-field Rayleigh fading model, which includes both line-of-sight (LoS) and non-line-of-sight (NLoS) components.
2. Detection rules and threshold derivation
Decision logic: Willie distinguishes between "Alice transmission (H₁)" and "Alice silence (H₀)" events by determining whether the received signal samples meet the criterion of "N or more samples with power exceeding the corresponding threshold."
✧  
Threshold Optimization: Derive a variable detection threshold ε(m) based on the Likelihood Ratio Test (LRT), which takes into account the time-varying interference from DRIS, distinguishing it from the fixed threshold in scenarios without DRIS.
3. Performance Metrics Definition
Detection performance: False alarm rate (FAR, the probability of misjudging H₁ when H₀ is present), and missed detection rate (MDR, the probability of misjudging H₀ when H₁ is present).
✧  
Communication Performance: Signal-to-Interference Noise Ratio (SJNR), reflecting the effective strength of Bob's received signal, with achievable rate R_b = log₂(1 + η_b).
4. Theoretical Analysis Method✧
Utilizing the Central Limit Theorem to derive the asymptotic Gaussian distribution characteristics of DRIS channels;
✧
Based on channel statistical characteristics and LRT to derive closed-form expressions for detection thresholds;
✧
Derive mathematical expressions for FAR and MDR, analyzing the asymptotic behavior of SJNR with respect to the number of DRIS units and transmit power.
5. Simulation Verification Settings✧
Key parameters: DRIS with 2048 reflective units, 1 bit quantization of the reflection coefficient, Alice's transmit power range -15~5 dBm, Willie takes M=5 samples in the coherent time, using the 3GPP standard for channel fading model.
✧
Comparative benchmarks: scenarios without DRIS, active jamming (AJ) scenarios, analyzing the influence of DRIS unit count, quantization precision, Alice-DRIS distance, and number of detection samples.
Conclusion 1  
The DRIS introduces full-passive interference (FPJ) through random time-varying reflection coefficients, which not only reduces Willie's FAR and MDR (improves detection accuracy) but also significantly interferes with Alice-Bob's concealed transmission—even if Willie misses detections, the DRIS can still disrupt communication quality through active channel aging (ACA) without needing to acquire Alice-Bob's channel information (CSI) or additional interference power.
2  
Increasing Alice's transmit power does not effectively improve communication performance: on one hand, SJNR will asymptotically converge to a constant value as the transmit power increases; on the other hand, higher transmit power will exacerbate the impact of DRIS interference and significantly increase Willie's detection probability.
3
Low-quantization accuracy DRIS can meet the requirements: A 1-bit quantized DRIS, when paired with a large number of reflective units, can effectively enhance Willie's detection accuracy while degrading Alice-Bob's communication performance. The DRIS should be as close to Alice as possible for maximizing interference and detection effects.
This paper reveals the significant threat of illegal RIS to covert communications, and future research needs to focus on countermeasures, such as signal classification/anomaly detection based on artificial intelligence and adaptive beamforming, to ensure the security of covert communications.
★

## Images

![(DRIS)Disruptive Detection and Recognition System! DRIS technology achieves synchronous detection and passive interference, without channel knowledge or additional power consumption. [Included MATLAB code]](01.jpg)
![(DRIS)Disruptive Detection and Recognition System! DRIS technology achieves synchronous detection and passive interference, without channel knowledge or additional power consumption. [Included MATLAB code]](02.jpg)
![(DRIS)Disruptive Detection and Recognition System! DRIS technology achieves synchronous detection and passive interference, without channel knowledge or additional power consumption. [Included MATLAB code]](03.jpg)
![(DRIS)Disruptive Detection and Recognition System! DRIS technology achieves synchronous detection and passive interference, without channel knowledge or additional power consumption. [Included MATLAB code]](04.jpg)
![(DRIS)Disruptive Detection and Recognition System! DRIS technology achieves synchronous detection and passive interference, without channel knowledge or additional power consumption. [Included MATLAB code]](05.jpg)
![(DRIS)Disruptive Detection and Recognition System! DRIS technology achieves synchronous detection and passive interference, without channel knowledge or additional power consumption. [Included MATLAB code]](06.jpg)
![(DRIS)Disruptive Detection and Recognition System! DRIS technology achieves synchronous detection and passive interference, without channel knowledge or additional power consumption. [Included MATLAB code]](07.jpg)
![(DRIS)Disruptive Detection and Recognition System! DRIS technology achieves synchronous detection and passive interference, without channel knowledge or additional power consumption. [Included MATLAB code]](08.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
