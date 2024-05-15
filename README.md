# One_Month_Wrist_PPG_Dataset

This dataset is described in the paper, One-Month Evaluation of Blood Pressure Estimation Using a Fine-Tuned Model with Wristband-Type Photoplethysmograms, accepted by IEEE Sensors Journal.<br />

### \<Overview\>
- This dataset contains 11 participant data (eight men, age: 31.1 ± 4.3 years; three women, age: 31.0 ± 11.3 years) over four days (one day per week) using a custommized wearable wristband-type PPG device. <br />
- Each day, the participants lay on their backs in a relaxed position in a row of well-cushioned chairs, during which the PPG was measured for six min in two sessions.
- The data structure is bellow:
  - __A/B/C+1/2/3/4__: participant ID<br />
    - week1/2/3/4    : week ID
      - session 1/2  : session ID
        - timestamp
          - ESPXXXXX(PPG-IMU) : raw data (you can use "PPG IR [-]", "SBP [mmHg]", and "DBP [mmHg]" for PPG2BP models)
          - processed         : 8-s segmented data (each row means 250 PPG samples, SBP, DBP, and HR)
          - processed_feature : 46-dimensional handcrafted features containing the amplitude. time, and area features
