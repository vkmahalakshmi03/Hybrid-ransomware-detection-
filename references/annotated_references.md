# Annotated References

20 papers reviewed. Annotations reflect how each study informed the hybrid detection model.

---

## Machine Learning and AI-Based Detection

**Ferdous et al. (2024)**  
*AI-Based Ransomware Detection: A Comprehensive Review*  
IEEE Access, vol. 12, pp. 136666–136695  
https://ieeexplore.ieee.org/document/10681072  
Most current comprehensive review in the dataset. Highlights the AI gap in unknown threat handling — confirmed that no single ML approach solves detection across all variant types. Directly supported the case for hybrid integration.

**Ispahany et al. (2024)**  
*Ransomware Detection Using Machine Learning: A Review, Research Limitations and Future Directions*  
IEEE Access, vol. 12, pp. 68785–68813  
https://ieeexplore.ieee.org/document/10521643  
Useful for understanding where ML-based detection breaks down. Identified dataset diversity and real-time latency as the two most cited limitations across reviewed ML studies.

**Smith, Khorsandroo & Roy (2022)**  
*Machine Learning Algorithms and Frameworks in Ransomware Detection*  
IEEE Access, vol. 10, pp. 117597–117610  
https://ieeexplore.ieee.org/document/9934917  
Framework-level comparison of ML approaches. Random Forest and Gradient Boosting emerged as the most operationally viable — balanced accuracy and compute cost better than deep learning alternatives.

**Masum et al. (2022)**  
*Ransomware Classification and Detection With Machine Learning Algorithms*  
IEEE CCWC 2022, pp. 316–322  
https://ieeexplore.ieee.org/document/9720869  
Tested ensemble classification for ransomware variant identification. Results supported the ensemble decision approach used in the hybrid model.

**Daku, Zavarsky & Malik (2018)**  
*Behavioral-Based Classification and Identification of Ransomware Variants Using Machine Learning*  
IEEE TrustCom/BigDataSE 2018, pp. 1560–1564  
https://ieeexplore.ieee.org/abstract/document/8456093  
Early ML behavioral classification study. Established that behavioral features — file access patterns, entropy changes — are reliable ML inputs for ransomware detection.

**Wan et al. (2018)**  
*Feature-Selection-Based Ransomware Detection with Machine Learning of Data Analysis*  
IEEE ICCCS 2018, pp. 85–88  
https://ieeexplore.ieee.org/abstract/document/8463300  
Showed that feature selection significantly impacts ML model performance. Informed which behavioral features to prioritize in the Stage 2 model design.

---

## Behavior-Based Detection

**Arabo et al. (2020)**  
*Detecting Ransomware Using Process Behavior Analysis*  
Procedia Computer Science, vol. 168, pp. 289–296  
https://www.sciencedirect.com/science/article/pii/S1877050920303884  
Process-level behavioral analysis — tracked file system calls and I/O rates. Confirmed that behavioral detection catches zero-day variants signature methods miss, but flagged high false positive rates as an unresolved operational problem.

**Madanayaka et al. (2023)**  
*A Proactive Approach for Behavior Based Ransomware Detection*  
IEEE ICAC 2023, pp. 346–351  
https://ieeexplore.ieee.org/abstract/document/10417620  
Proactive alerting based on behavioral anomalies. Aligned with the dynamic analysis component of the hybrid model — monitoring for mass encryption and unauthorized file access before damage spreads.

**Ahmad et al. (2023)**  
*A Recent Systematic Review of Ransomware Attack Detection in Machine Learning Techniques*  
IEEE AiDAS 2023, pp. 349–354  
https://ieeexplore.ieee.org/document/10284709  
Systematic review covering ML-based behavioral approaches. Useful for identifying which behavioral features appear most consistently across detection studies.

---

## Network Behavior-Based Detection

**Srivastava et al. (2023)**  
*Ransomware Detection Based on Network Behavior Using ML and Hidden Markov Model*  
IEEE CSR 2023, pp. 227–233  
https://ieeexplore.ieee.org/document/10225001  
Applied Hidden Markov Models to network traffic patterns. Relevant to the C2 communication detection component — encrypted channel behavior as a ransomware indicator.

**Teymourlouei & Harris (2021)**  
*Detecting Ransomware Automated Based on Network Behavior Using Machine Learning*  
IEEE CSCI 2021, pp. 728–734  
https://ieeexplore.ieee.org/document/9798937  
Network-layer ML detection. Demonstrated that C2 communication patterns are detectable before encryption begins — early detection window that behavioral file-system monitoring alone misses.

---

## Deep Learning Approaches

**Sharma, Batra & Malik (2024)**  
*A Comparative Study of Malware Detection Using Hybrid Deep Learning Techniques*  
IEEE ICETSIS 2024, pp. 1260–1266  
https://ieeexplore.ieee.org/document/10459638  
Compared hybrid deep learning architectures. Results confirmed deep learning outperforms traditional ML on accuracy but at compute costs that limit real-time applicability.

**Al-Hawawreh & Sitnikova (2019)**  
*Leveraging Deep Learning Models for Ransomware Detection in the IIoT Environment*  
IEEE MilCIS 2019, pp. 1–6  
https://ieeexplore.ieee.org/document/8930732  
IIoT-specific deep learning detection. Highlighted the resource constraint problem — deep learning is impractical in low-compute environments, which shaped the decision to use Random Forest and Gradient Boosting over neural networks.

**Charmilisri et al. (2023)**  
*A Novel Ransomware Virus Detection Technique Using Machine and Deep Learning Methods*  
IEEE ICICCS 2023, pp. 8–14  
https://ieeexplore.ieee.org/document/10142938  
Combined ML and deep learning for detection. One of the few papers testing hybrid ML architectures — results supported ensemble approaches over single-model designs.

---

## Cloud and Scalability

**Aslan, Ozkan-Okay & Gupta (2021)**  
*Intelligent Behavior-Based Malware Detection System on Cloud Computing Environment*  
IEEE Access, vol. 9, pp. 83252–83271  
https://ieeexplore.ieee.org/document/9448102  
Cloud-deployed behavioral detection at scale. Validated that behavioral analysis can run in cloud infrastructure without prohibitive latency — directly relevant to the scalability design rationale.

---

## Hybrid and Evolutionary Approaches

**Aljubory & Khammas (2021)**  
*Hybrid Evolutionary Approach in Feature Vector for Ransomware Detection*  
IEEE ITSS-IoE 2021, pp. 1–6  
https://ieeexplore.ieee.org/document/9615344  
Evolutionary feature selection for hybrid detection. Showed that optimized feature vectors improve hybrid model accuracy — informed the behavioral feature prioritization in Stage 2.

---

## Blockchain Integration

**Singh et al. (2022)**  
*Blockchain: Tool for Controlling Ransomware Through Pre-Encryption and Post-Encryption Behavior*  
IEEE CCICT 2022, pp. 584–589  
https://ieeexplore.ieee.org/document/9913615  
Blockchain for ransomware audit trails and pre/post-encryption behavior logging. Relevant to the forensic traceability component discussed in the hybrid model architecture.

**Aneja et al. (2021)**  
*Malware Mobile Application Detection Using Blockchain and Machine Learning*  
IEEE GCAT 2021, pp. 1–7  
https://ieeexplore.ieee.org/document/9587880  
Blockchain + ML for mobile malware detection. Explored blockchain's role in immutable logging — applicable to the audit trail design in the hybrid model.

**Blockchain-Based Semi-Autonomous Ransomware (2020)**  
Future Generation Computer Systems, vol. 112, pp. 589–603  
https://www.sciencedirect.com/science/article/abs/pii/S0167739X19317406  
Adversarial perspective — how ransomware can leverage blockchain. Understanding attacker-side blockchain use informed the detection model's approach to encrypted C2 channel identification.

**Patel et al. (2024)**  
*Effective Intrusion Detection and Prevention System of Botnet Attack in Blockchain Technology Using RNN*  
IEEE CISCON 2024, pp. 1–6  
https://ieeexplore.ieee.org/document/10696133  
RNN-based detection in blockchain environments. Peripheral to the core ransomware detection focus but relevant to the broader threat detection architecture discussion.
