
# EXPERIMENT 4
# NAME  : MONICA G
# REGNO : 212224040198

## ASSET-ORIENTED RISK ASSESSMENT OF STORAGE ASSETS IN AWS 

---

## Aim

To identify storage assets in **AWS S3**, identify possible vulnerabilities and threats, and assess their likelihood, impact, and risk level.

---

## Software / Cloud Services Required

- AWS Account
- Microsoft Azure Account
- Web Browser
- Internet Connection

### Cloud Services Used

| Cloud Platform | Storage Service |
|---|---|
| AWS | Amazon S3 |

---

# PART A — AWS S3 STORAGE ASSESSMENT

## Step 1: Login to AWS

1. Open the AWS Management Console.
2. Sign in using your AWS account.
3. Search for **S3**.
4. Select **Amazon S3**.

---

## Step 2: Select the S3 Bucket

1. Click **Buckets**.
2. Select the S3 bucket created in the previous experiment.
3. Record:
   - Bucket name
   - AWS Region
   - Number/type of objects

<img width="1915" height="1076" alt="image" src="https://github.com/user-attachments/assets/f164b90f-882d-4ff4-9165-5de096c3442c" />

---

## Step 3: Check Block Public Access

1. Open the S3 bucket.
2. Select **Permissions**.
3. Locate **Block public access (bucket settings)**.
4. Check **Block all public access**.

### Record

- **ON** → Secure configuration
- **OFF** → Potential public-access risk

<img width="1906" height="1022" alt="image" src="https://github.com/user-attachments/assets/be23a232-7e15-4553-977f-cf6e77366672" />


---

## Step 4: Check Bucket Versioning

1. Select the **Properties** tab.
2. Locate **Bucket Versioning**.
3. Record whether it is:
   - Enabled
   - Disabled

### Security Purpose

Versioning helps recover previous versions of objects after accidental deletion or modification.

<img width="1903" height="810" alt="image" src="https://github.com/user-attachments/assets/46174071-3822-43db-bfd2-e1e1deb1b25e" />


---

## Step 5: Check Default Encryption

1. Stay in the **Properties** tab.
2. Locate **Default encryption**.
3. Record the encryption type.

### Possible Configurations

- SSE-S3
- SSE-KMS
- DSSE-KMS

### Security Purpose

Encryption protects stored data from unauthorized disclosure.

<img width="1907" height="1092" alt="image" src="https://github.com/user-attachments/assets/1c544e30-5370-41e0-9dea-7f073f2143a7" />


---

## Step 6: Check Bucket Policy

1. Select **Permissions**.
2. Locate **Bucket policy**.
3. Check whether a bucket policy exists.

### Record

- Policy exists
- No policy

> **Note:** A missing bucket policy is not automatically a vulnerability. Access may be controlled through IAM and other AWS security mechanisms.

<img width="1911" height="1073" alt="image" src="https://github.com/user-attachments/assets/74c21415-ab3f-4adc-b2eb-4ede9cc267f2" />



---

## Step 7: Check Object Ownership and ACL

1. In **Permissions**, locate **Object Ownership**.
2. Record the current configuration.

A common secure configuration is:

**Bucket owner enforced**

This means:

- ACLs are disabled.
- Objects are owned by the bucket owner.
- Access is controlled using policies.

<img width="1910" height="997" alt="image" src="https://github.com/user-attachments/assets/e1c0bc0b-d1c8-4dfe-80f1-06fd9cd98463" />


---
## Step 8: Check Server Access Logging

1. Go to **Properties**.
2. Locate **Server access logging**.
3. Record whether it is:
   - Enabled
   - Disabled

### Security Purpose

Logging helps investigate suspicious or unauthorized access to the bucket.

<img width="1917" height="1085" alt="image" src="https://github.com/user-attachments/assets/b865dfd5-e757-4da5-9c56-c5874f7c896c" />

---


## Step 9: Check Object Ownership and ACL

1. In **Permissions**, locate **Object Ownership**.
2. Record the current configuration.

A common secure configuration is:

**Bucket owner enforced**

This means:

- ACLs are disabled.
- Objects are owned by the bucket owner.
- Access is controlled using policies.

<img width="1913" height="1085" alt="image" src="https://github.com/user-attachments/assets/af90e501-e83a-4930-ac82-73f1830d921a" />

---


---

# PART B — AWS RISK ASSESSMENT

After checking the S3 configuration, identify possible vulnerabilities and threats.

## Risk Formula

**Risk Score = Likelihood × Impact**

### Likelihood Scale

| Score | Description |
|---:|---|
| 1 | Very Low |
| 2 | Low |
| 3 | Medium |
| 4 | High |
| 5 | Very High |

## AWS Risk Assessment

> Students must use their actual configuration while preparing the final table.

| Asset | Vulnerability | Threat | Likelihood | Impact | Risk Score | Risk Level | Recommended Mitigation |
|---|---|---|---:|---:|---:|---|---|
| S3 Bucket | Versioning disabled | Accidental/malicious data deletion | 3 | 4 | 12 | High | Enable versioning |
| S3 Bucket | Access logging disabled | Difficult investigation of unauthorized activity | 3 | 3 | 9 | Medium | Enable appropriate logging |
| S3 Bucket | Public access enabled | Unauthorized data access | 4 | 5 | 20 | Critical | Enable Block Public Access |
| S3 Bucket | Weak access permissions | Unauthorized modification/access | 3 | 4 | 12 | High | Apply least privilege |

---

Risk scores were calculated using the **Likelihood × Impact** method, and appropriate security mitigation measures were recommended.


## Result

~~~
AWS S3 security configurations were analyzed and potential risks were identified.
Risk levels were assessed and suitable security measures were recommended. 
~~~
