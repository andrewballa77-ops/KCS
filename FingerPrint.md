# Detailed Experimental Methodology for Evaluating User Convenience of Your Fingerprint Password Generator

For your research, I recommend treating user convenience as a measurable scientific outcome, rather than simply asking users whether they like the device.

Your research should answer four central questions:

1. Is fingerprint-based password generation faster than conventional password entry?
2. Does the small fingerprint sensor make authentication more difficult?
3. How much inconvenience is caused by failed fingerprint scans and repeated attempts?
4. Does your device reduce user workload and improve overall satisfaction?

Your device is particularly interesting because it combines a 96 × 112-pixel fingerprint sensor, a 160 MHz GD32 Cortex-M3 processor, deterministic password generation, USB keyboard emulation, and an estimated hardware cost of $15.

## 1. Scientific framework for evaluating convenience

According to ISO 9241-11, usability is evaluated through effectiveness, efficiency, and satisfaction in a specified context of use.

For your research, these can be expanded into six measurable dimensions.

| Dimension             | Research question                     | Primary indicator             |
| --------------------- | ------------------------------------- | ----------------------------- |
| Effectiveness         | Can users complete authentication?    | Task success rate             |
| Efficiency            | How quickly can users authenticate?   | Total login time              |
| Physical convenience  | Is the small sensor easy to touch?    | Repositioning and retry count |
| Cognitive convenience | Is authentication mentally demanding? | NASA-TLX                      |
| Satisfaction          | Do users prefer the device?           | SUS score                     |
| Learnability          | Does usage become easier over time?   | Learning curve                |

These should be evaluated separately because a device can be fast but frustrating, or highly reliable but slow.

## 2. Authentication time: detailed evaluation

You currently report a fingerprint processing time of 256 ms. This is a useful technical performance indicator, but it is not the complete user experience.

A person must find the sensor, position their finger, wait for processing, and wait for the password to be entered.

## Authentication timeline

1. Start of login task

   Researcher presents the login screen and gives a start signal
2. Finger placement

   User locates the sensor and positions their finger
3. Fingerprint acquisition and processing

   Device captures the fingerprint and processes biometric information
4. Password derivation

   The device computes the deterministic password
5. USB HID output

   The device enters the generated password into the login field
6. Authentication completed

   The test application confirms a successful login

Define:

\\[ T\_{\text{total}}=t\_{\text{success}}-t\_{\text{start}} \\]

This end-to-end measurement includes user interaction, device processing, retries, and host response.

### Measurement equipment

You can use:

- A Python or JavaScript test application to record start and completion timestamps.
- Firmware timestamps to measure processing and password generation.
- A USB HID event logger to measure typing duration.
- A video camera for analyzing finger placement and repositioning time.

Synchronize timestamps across measurement systems, or use one host clock for end-to-end measurements.

### Example of collected data

Illustrative data, not experimental results

| Participant | Login 1 | Login 2 | Login 3 | Average |
| ----------- | ------- | ------- | ------- | ------- |
| P01         | 1.5 s   | 1.2 s   | 1.1 s   | 1.27 s  |
| P02         | 2.3 s   | 1.8 s   | 1.6 s   | 1.90 s  |
| P03         | 1.4 s   | 1.3 s   | 1.2 s   | 1.30 s  |

Report the median, mean, standard deviation, and 95th percentile. The 95th percentile is important because users often remember unusually slow authentication experiences.

## 3. Authentication success and retry inconvenience

Your reported True Acceptance Rate is 90%. If this is measured at a fixed decision threshold, the corresponding False Rejection Rate is 10%.

However, for user convenience, the important question is not only whether the fingerprint is recognized, but whether the user successfully completes the login task.

### Three separate indicators

A. First-attempt success rate

\\[ FASR=\frac{N\_{\text{successful first attempts}}}{N\_{\text{total login tasks}}}\times100\\% \\]

B. Task completion rate

\\[ TCR=\frac{N\_{\text{completed login tasks}}}{N\_{\text{total login tasks}}}\times100\\% \\]

Define a fixed task limit, such as three fingerprint attempts or 15 seconds.

C. Retry burden

\\[ RB=\frac{\sum\_{i=1}^{N}\max(0,A_i-1)}{N} \\]

Where \\(A_i\\) is the number of attempts made during login task \\(i\\).

A retry burden of 0.2 means users require, on average, 0.2 additional fingerprint scans per login task.

### Interactive example: effect of first-attempt success

First-attempt success probability

## 90%

Time per attempt

### 1.5 s

Expected attempts

# 1.11

Expected login time

# 1.67 s

Illustrative geometric model assuming independent attempts, constant success probability, no retry overhead, and unlimited attempts. Actual measurements may differ substantially.

The experiment should also measure whether repeated failures cause users to press harder, reposition their finger, or abandon the task.

## 4. Small-area fingerprint convenience: experimental design

This is one of the most valuable research directions for your device.

A small sensor captures only a limited portion of the fingerprint. Consequently, the user may need to position their finger more precisely.

You should evaluate finger placement tolerance, rotation tolerance, contact pressure, and finger condition.

[Capacitive Fingerprint Reader (ID809, SAMD21) — Maker Portal](https://images.openai.com/static-rsc-4/NaVevuqty0CZ1BdAskQPL7IKqW7n3-prQPzXP-5c-koigFuTTyXeMf6Z30ba3p3w-oER6ez6j7Ryk3QVyDeFKcjObsPp79TGP5WDyQxkEzRt03SWL_QrCmJ6I_faoVlc-lIMaT4hE5m0n5ePPu1RIuOQbHr5pkTLr82ElMR0RGA?purpose=inline)

Normal placement

Finger centered on the sensing area

[Fingerprint-Based Payment Lands On Korean Android Smartphone](https://images.openai.com/static-rsc-4/kS0WeIWiUTIoLWTSSosZXcC8_Fb5FIm1ZG3Sl4Pam3vsyapAxq7y7ZyrzGNdeufE2ObI60QNWPhB0Dpvy-geKCny688W1_vxvfsqu-RyLqHYMK3GSTuObokudB9CxBtYd5JNKnUFlW0MIO7NnIUPEottttBnsesD2kptTLtwA8w?purpose=inline)

Partial placement

Only part of the sensing area is covered

### Experiment A: Finger displacement

Ask participants to place their finger at five controlled positions:

- Center
- Left offset
- Right offset
- Upper offset
- Lower offset

Measure success rate, authentication time, and repositioning count for each condition.

### Experiment B: Finger rotation

Test five finger orientations: −20°, −10°, 0°, +10°, and +20°.

For each angle, collect repeated scans and calculate:

\\[ SR(\theta)=\frac{N\_{\text{successful at angle }\theta}}{N\_{\text{attempts at angle }\theta}}\times100\\% \\]

This produces a rotation tolerance curve, which can be compared with other small-area fingerprint recognition algorithms.

### Experiment C: Finger condition

Evaluate dry, normal, and slightly moist fingers under controlled, safe conditions. Do not assume these conditions are equivalent to normal day-to-day usage; record how they are produced.

For all three experiments, distinguish recognition failure from password reconstruction failure. Your device must reproduce the correct password, not merely accept the fingerprint.

## 5. Password reproducibility as a convenience indicator

Your device is unusual because the same fingerprint is intended to generate the same password without storing the password.

This creates an additional convenience requirement: password stability.

Define the Password Reproducibility Rate:

\\[ PRR=\frac{N\_{\text{correctly reproduced passwords}}}{N\_{\text{valid genuine attempts}}}\times100\\% \\]

For example, if 1,000 valid genuine attempts produce 970 correct passwords:

\\[ PRR=97\\% \\]

That would be a hypothetical 97% reproducibility rate.

For your device, I recommend measuring:

| Indicator                        | Meaning                                                |
| -------------------------------- | ------------------------------------------------------ |
| Password reproducibility rate    | Same enrolled finger produces expected password        |
| Cross-finger collision rate      | Different fingers produce identical passwords          |
| Password generation failure rate | Processing succeeds but no valid password is generated |
| Password output correctness      | USB HID enters the intended password exactly           |
| Password recovery burden         | Time required when a password cannot be reproduced     |

These indicators are especially relevant because a password that changes unexpectedly can prevent a user from accessing their account.

Also, the absence of stored templates does not automatically guarantee password security. Biometric entropy, password predictability, and protection against compromised host computers require separate analysis.

## 6. Measuring user satisfaction with SUS

The System Usability Scale (SUS) is a standardized questionnaire with 10 items.

Participants respond using a five-point scale:

1 = Strongly disagree, 5 = Strongly agree.

Below is an interactive SUS questionnaire for one participant, using the standard item wording.

SUS questionnaire

0/10 answered

1 = Strongly disagree · 5 = Strongly agree

1\. I think that I would like to use this system frequently.

1

2

3

4

5

2\. I found the system unnecessarily complex.

1

2

3

4

5

3\. I thought the system was easy to use.

1

2

3

4

5

4\. I think that I would need the support of a technical person to be able to use this system.

1

2

3

4

5

5\. I found the various functions in this system were well integrated.

1

2

3

4

5

6\. I thought there was too much inconsistency in this system.

1

2

3

4

5

7\. I would imagine that most people would learn to use this system very quickly.

1

2

3

4

5

8\. I found the system very cumbersome to use.

1

2

3

4

5

9\. I felt very confident using the system.

1

2

3

4

5

10\. I needed to learn a lot of things before I could get going with this system.

1

2

3

4

5

Calculated SUS score

# — / 100

Complete all 10 responses to calculate the score.

&#x20;Reset Copy results

Calculate the SUS score using:

\\[ SUS=2.5\left[\sum\_{\text{odd }i}(R_i-1)+\sum\_{\text{even }i}(5-R_i)\right] \\]

A score of approximately 68 is often used as a general reference point, but it is not a universal pass/fail standard. Compare your device with the other authentication methods tested in the same study.

## 7. Evaluating user workload using NASA-TLX

NASA-TLX provides six dimensions for measuring perceived workload.

| Dimension       | What it means for your device                    |
| --------------- | ------------------------------------------------ |
| Mental demand   | Effort needed to understand the login process    |
| Physical demand | Effort required to position and press the finger |
| Temporal demand | Feeling of being rushed or delayed               |
| Performance     | User's perception of task success                |
| Effort          | Overall work required to complete login          |
| Frustration     | Irritation caused by repeated failures           |

For an initial experiment, use Raw TLX, the unweighted average of six ratings on a 0–100 scale, with appropriate scoring direction.

\\[ RTLX=\frac{1}{6}\sum\_{i=1}^{6}R_i \\]

Lower scores generally indicate lower workload. Record the six dimensions individually, because a device may have low mental demand but high physical demand.

## 8. Learnability and long-term convenience

Users may initially struggle with the small sensor but improve after practice.

Measure authentication time and retry count across multiple sessions.

Example learning curve

0 s0.75 s1.5 s2.25 s3 sSession 1Session 2Session 3Session 4Session 5

Hypothetical results illustrating the expected analysis, not measured device performance.

A possible protocol is five sessions across one or two weeks. Collect 20 login attempts per participant per session.

Calculate learning improvement as:

\\[ LI=\frac{T\_{\text{first}}-T\_{\text{last}}}{T\_{\text{first}}}\times100\\% \\]

A positive value indicates reduced completion time.

You should also assess whether users remember how to operate the device after several days without practice.

## 9. Complete experimental plan for your SCI paper

## Recommended research protocol

| Participants           | 40–60, subject to power analysis                         |
| ---------------------- | -------------------------------------------------------- |
| Authentication methods | Your device, manual password, password manager autofill  |
| Login attempts         | 30 per method per participant per session                |
| Sessions               | 3–5 sessions on separate days                            |
| Sensor tests           | Placement, rotation, pressure, finger condition          |
| Objective measures     | Time, success, retries, HID errors                       |
| Subjective measures    | SUS, NASA-TLX, preference                                |
| Statistical analysis   | Mixed-effects models, confidence intervals, effect sizes |

A within-subject comparison is particularly useful because each participant can evaluate all three methods. Randomize or counterbalance the order to reduce learning and fatigue effects.

For ethical and scientific validity, obtain informed consent, avoid collecting real account passwords, and minimize biometric data retention. If raw fingerprints are collected, follow your institution's biometric data protection and ethics requirements.

## 10. How to determine whether your device is genuinely more convenient

Your final paper should not depend on a single performance number.

For example, your device might have a fast 256 ms processing stage but require multiple finger placements. In that case, total authentication time and frustration could be worse than password manager autofill.

I recommend establishing three primary hypotheses:

- H1: Your device reduces end-to-end login time compared with manual password entry.
- H2: Your device achieves higher perceived usability (SUS) than manual password entry.
- H3: Small-area finger placement variation significantly affects first-attempt success and retry burden.

Then evaluate secondary outcomes such as password reproducibility, physical workload, and learning effects.

A successful paper can report both advantages and limitations. It does not need to show that your device outperforms every alternative.

## 11. Recommended scientific title and contribution

Proposed title:

“A Comprehensive Usability and Performance Evaluation of a Low-Cost Small-Area Fingerprint-Based Password Generation Device”

Your paper could make three contributions:

1. A reproducible experimental framework for measuring convenience in fingerprint-derived password systems.
2. Quantitative evidence of the relationship between small-area fingerprint acquisition, retry burden, and user experience.
3. A comparison of low-cost biometric password generation with conventional password authentication methods.

My recommendation: Begin with a pilot study of 10 participants to validate the logging software, task definitions, and questionnaire procedure. Then use the pilot's variability estimates to plan the main experiment.

The most important scientific distinction is to measure successful password-based login, not just successful fingerprint recognition. That is what makes your research specific to the device you developed.