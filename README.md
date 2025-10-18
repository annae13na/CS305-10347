# CS 305 Module Eight Journal  
**Author:** Anna Fuentes  
**Course:** CS-305 – Software Security  
**Artifact:** Artemis Financial Practices for Secure Software Report  


## 1. Client Summary
Artemis Financial is a financial services company that develops custom software to handle sensitive customer and financial data. The client requested secure communication protocols and practices to protect customer information during transmission and storage. The company also wanted to ensure that its software complied with secure development standards, vulnerability assessments, and DevSecOps best practices.


## 2. What I Did Well
I effectively implemented secure communication using HTTPS with a self-signed SSL certificate, deployed a SHA-256 hashing function for data integrity, and selected AES as the preferred cipher for encryption. I also conducted a successful OWASP Dependency-Check to confirm that no critical vulnerabilities existed after refactoring.  

Secure coding practices like encryption, hashing, and dependency scanning are vital for maintaining trust and preventing breaches. They protect financial data and ensure the company meets industry security and compliance standards.


## 3. Challenges and Learning
The most challenging aspect was correctly configuring SSL within the Spring Boot application and understanding the interaction between certificates, keystores, and encrypted communication. Through this process, I learned how to use **Java Keytool** to generate and manage certificates and how to verify HTTPS deployment using Tomcat.  

Integrating the **OWASP dependency scanner** also deepened my understanding of how to verify libraries against known vulnerabilities and maintain a secure build pipeline. As Freeman (2022) explains, secure SDLC processes must “shift everywhere,” embedding security at all phases of development.

## 4. Increasing Layers of Security
Multiple security layers were implemented throughout this project:
- **AES cipher** for data confidentiality and encryption.  
- **SHA-256 hashing** to verify data integrity.  
- **Self-signed SSL certificate** for HTTPS communication.  
- **OWASP Dependency-Check** to detect vulnerabilities in dependencies.  
- **Secure configuration and least-privilege principles** to reduce risk exposure.  
In future projects, I plan to expand on these by adding dynamic testing (DAST), automated CI/CD scans, and periodic certificate rotation to further strengthen security posture.


## 5. Functionality and Verification
After implementing the changes, I executed the **SslServerApplication.java** in Eclipse. The console output confirmed successful initialization with:  
> *Tomcat started on port(s): 8443 (https)*  
The browser successfully displayed the hashed output from the `/hash` endpoint, verifying both secure communication and functional accuracy. The OWASP dependency scan also confirmed no new vulnerabilities were introduced after refactoring, validating both security and functionality.


## 6. Tools and Practices for Future Use
Key tools and practices I will carry forward include:
- **Java Keytool** – for managing digital certificates and keystores.  
- **OWASP Dependency-Check (Maven plugin)** – for automated vulnerability scanning.  
- **Spring Boot SSL Configuration** – for secure HTTPS deployment.  
- **AES and SHA-256 Cryptography** – for encryption and data integrity verification.  
- **NIST and OWASP guidelines** – for aligning development practices with federal and industry security standards.  

These tools will continue to support my ability to identify, mitigate, and verify software vulnerabilities in future DevSecOps workflows.

## 7. Portfolio Value
This artifact highlights my ability to implement end-to-end secure software practices—from cryptographic implementation to vulnerability assessment. It demonstrates skills in:
- Secure coding and encryption techniques  
- Certificate management and HTTPS deployment  
- Automated vulnerability scanning  
- DevSecOps process integration  
Future employers will see that I can apply cybersecurity principles directly to software design and deployment, ensuring data protection, compliance, and reliability in enterprise environments.


## 8. References
Allodi, L., Cremonini, M., Massacci, F., & Shim, W. (2018). *The effect of security education and expertise on security assessments: The case of software vulnerabilities.* arXiv:1808.06547 [cs.CY]. https://arxiv.org/abs/1808.06547  

Freeman, C. (2022, August 8). *Secure SDLC 101: Mastering software development life cycle security.* Black Duck Software. https://www.blackduck.com/  

National Institute of Standards and Technology. (2001). *Announcing the Advanced Encryption Standard (AES)* (FIPS Publication No. 197). https://doi.org/10.6028/NIST.FIPS.197  

Open Web Application Security Project. (2023). *OWASP Dependency-Check Documentation.* https://owasp.org/www-project-dependency-check/  

Oracle. (2024). *keytool – Key and Certificate Management Tool.* https://docs.oracle.com/en/java/javase/17/docs/specs/man/keytool.html  

Spring Boot. (2024). *Spring Boot Reference Documentation – Securing a Web Application.* https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#web.security  

OpenText. (2025, October 14). *Delivering contextual AI: Unlocking trusted and secure information management with CE 25.4.* OpenText Blogs. https://blogs.opentext.com/  

U.S. Department of Commerce. (2022). *National Vulnerability Database (NVD).* https://nvd.nist.gov/  
