# Fleming

## What is Fleming? <a href="#what-is-fleming" id="what-is-fleming"></a>

#### [Try Demo App](https://emr.hippocrades.com) <a href="#try-demo-app" id="try-demo-app"></a>

Hippocrades is exposed as a set of comprehensive healthcare APIs covering crucial medical information such as patients, medical records, diagnostic test results, and so on. These APIs collectively form Fleming.

Fleming APIs have been developed to form the backbone of health-tech products for doctors, clinics, hospitals, pharmacies, and other health facilities, capturing important business logic cross-connecting all these different sources of medical information with each other.

These APIs are exposed as well-documented REST endpoints, promoting interoperability with any modern information system. Even legacy information systems may connect to HAPI Hub and begin storing on the Health Information Exchange by developing a thin REST client layer on top of their existing architecture, driving the potential for market acceptance even higher.

![](../.gitbook/assets/hippocrades-fleming.png)

## Available API Services <a href="#available-api-services" id="available-api-services"></a>

* Electronic Medical Records
* Personal Details
* Queuing
* Appointments
* Pharmacy
* Billing
* Laboratory
* Imaging
* Physical Medical Exam (PME)
* Ward Management
* Authentication & Authorization
* SMS
* Chat
* Notification
* Disbursement
* Payment gateways
* PRM
* Metrics

## Security / Privacy / Compliance Features <a href="#security--privacy--compliance-features" id="security--privacy--compliance-features"></a>

* 2FA Authentication
* Encryption by default, at rest and in-transit
* Industry-standard encryption algorithms (AES256)
* Data hashing for integrity checks
* Disassociated records
* Audit logs
* Privileged access management
* Adheres to HIPAA guidelines

## System Agnostic <a href="#system-agnostic" id="system-agnostic"></a>

Fleming is system agnostic, allowing any system to easily integrate with it. In doing so, an existing EHR system can utilize HAPI Hub’s API endpoints to avail of its different services, as mentioned above. As such, EHR System or Health Platform Providers can also add modules and functionalities using HAPI Cure’s front-end solutions or create their Custom App from scratch using the services provided by the APIs.

![](<../.gitbook/assets/image (2).png>)

## Ownership <a href="#ownership" id="ownership"></a>

Ownership and privilege-based access are first-class concerns in Fleming’s architecture in its effort to maintain privacy even while promoting interoperability. In fact, the system is even architected to dissociate personally identifiable information (PII) from protected health information (PHI) via encryption.

Even with these safeguards, however, there are still cases where different parties must verify health information, and traditionally there would be no other way to accomplish this than to share the health information in question. Privacy concerns in these cases are mitigated by strict privacy compliance legislation, but it doesn’t change the fact that there are different eyes on the health information in question. Not to mention that privacy compliance in this way is based on trust – that the third parties are not secretly taking advantage of access to patients’ health information.

This is where Nightingale blockchain comes in, using the novel concept of zero-knowledge proofs to accomplish completely private information exchange.

## Status: DONE <a href="#status-done" id="status-done"></a>

Fleming is already existing and functional. Curie’s backend is primarily using Fleming. One can check the available APIs at [Fleming APIs](https://docs.hapihub.com).
