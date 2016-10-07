---
layout: default
title: CRLs And Certificates
permalink: /crls/
---
<div style="float:right; padding:10px; margin-right:20px; border-radius:10px; width:180px; height:40px; box-shadow:3px 3px 5px 0px; text-align:center; background-color:#CCC; color:#666666">
<div style="color:#000000">
<em>Introduction</em>
</div>
</div>

This section will help you quickly understand the basics of Federal PKI certificates, certificate policy, and certificate revocation lists (CRLs). This section will also provide you with commonly requested Federal PKI links.

1. [What are Certificates?](#public-key-certificates) 
2. [What is a Certificate Policy?](#certificate-policy)
3. [What are Certificate Revocation Lists (CRLs)?](#certificate-revocation-lists)
4. [Links to Commonly Requested Federal PKI CRLs and Certificates?](#federal-pki-crls-and-certificates)
5. [Where can I find the Federal Certificate Policies?](#federal-pki-certificate-polices-and-profiles)

### What are Certificates ###

![Example of certificate fields](https://raw.githubusercontent.com/djpackham/fpki-guides/gh-pages/img/certFields.png){:style="float:right"}

Certificates are files that can be used for gaining access to networks, applications, digitally signing, encrypting, or creating trusted connections. You can review [Details of a PIV Credential](https://gsa.github.io/piv-guides/details/) to learn more about viewing, exporting and understanding PIV certificates. You can also review the [HTTPS-Only Standard](https://https.cio.gov/certificates/) to learn more about certificates use in HTTPS connections.

A certificate can be issued to a person or a device. A certificate includes information about the person/device, the issuer of the certificate, the purpose(s) of the certificate, and other information to verify if the certificate is valid. See the image to the right for an example of the common fields/values you'd find in a certificate.

Similar to a paper certificate, certificates are made valid when they are signed by a recognized and trustworthy authority, known as a Certificate Authority (CA). Learn more about Certificate Authorities by viewing the [Certificate Authorities Page](/ca/). Also learn more about the different types of certificates by reviewing the [What are the Different Types of Certificates and their Purpose page](/pki/).

### What is a Certificate Policy ###

![Example of certificate fields](https://raw.githubusercontent.com/djpackham/fpki-guides/gh-pages/img/certPolicy.PNG){:style="float:right"}

Certificate are not all used for the same reason or issued by the same Certificate Authority. Some certificates may be used for digitally signing a document, another certificate may be used for logging into a website. In simple terms, we can say that a certificate policy is a set of rules used to define the use a certificate.

Similar to other Public Key Infrastructures, the Federal PKI has defined their rules for certificates or certificate policies, in a document called X.509 Certificate Policy For The U.S. Federal PKI Common Policy Framework. This document includes much more than just the 10 defined set of certificate policies. It also include the architecture, procedures, controls, audits, etc., related to running the Federal PKI.

An example of a certificate policy is demonstrated to the right. If you lookup this policy in the Federal PKI Certificate Policy doc, you'll see that the policy identifier is mapped to *id-fpki-common-policy*

The Federal PKI helps create best-practice technical, operating, and policy requirements.  Much of that material directly addresses two essential PKI elements: 

- **Certificates**; and 
- **Certificate Revocation Lists** (almost always referred to as CRLs)

The degree to which a Relying Party can rely on (trust) a certificate for any purpose depends upon the policies associated with that certificate. Then,   as long as a certificate is valid (not expired, not revoked, legitimate CA signature), the certificate can be relied upon and used for its intended purpose(s). 

> The more strict the certificate policy associated with the certificate, the more a Relying Party can trust the certificate.  

### What are Certificate Revocation Lists ###
Various events can occur that require a certificate (or a set of certificates) to no longer be trusted.  When those events occur, the certificate needs to be revoked and Relying Parties notified,  Examples of such events include:

- Lost, stolen, damaged, or misused certificate.  
- Compliance issues with or a security breach of the Certification Authority that issued the certificate.  
- Termination of employment of certificate holder.
- Certificate holder switches to a different job role (e.g., switching from Role A to Role B, and the certificate is designated for use only by Role A), 
- Certification Authority that issued the certificate terminates its relationship with the Federal PKI.

> In technical terms, *a certificate should be revoked when the binding between the subject and the subject’s public key defined within a certificate is no longer considered valid*.

To notify Relying Parties of revoked certificates, CAs publish Certificate Revocation Lists (CRLs), which are simple lists of certificates that have been revoked and should no longer be relied upon.  

> Relying Parties Parties should obtain CRLs on an ongoing basis and process them accordingly. CAs publish CRLs on a regular schedule and on an emergency basis - as specified by applicable certificate policy.

> To help Relying Parties find CRLs, CAs make public both a description of how to obtain revocation information for the certificates they publish and an explanation of the consequences of using out of date revocation information.  

### Illustration of a Certificate and CRL ###

<img src="/img/crls_diagram1.jpg"/>

### Downloadable Federal PKI CRLs and Certificates ###
* ***Federal Common Policy Certification Authority (Common or FCPCA)***

     * [Common CA Root Certificate](http://http.fpki.gov/fcpca/fcpca.crt)

     * [CRL](http://http.fpki.gov/fcpca/fcpca.cr) 

     * FCPCA DN:  **cn=Federal Common Policy CA, ou=FPKI, o=U.S. Government, c=US** 

     * sha1 Thumbprint: **90 5f 94 2f d9 f2 8f 67 9b 37 81 80 fd 4f 84 63 47 f6 45 c1**

     * [P7Cs (Issued By)](http://http.fpki.gov/fcpca/caCertsIssuedByfcpca.p7c)

     * [P7Cs (Issued To):](http://http.fpki.gov/fcpca/caCertsIssuedTofcpca.p7c)

* ***Federal Bridge Certification Authority (Bridge or FCPCA)***

     * [FBCA CRL](http://http.fpki.gov/bridge/fbca.crl)

     * [FBCA2013 CRL](http://http.fpki.gov/bridge/fbca2013.crl)    

     * [P7Cs (Issued By)](http://http.fpki.gov/bridge/caCertsIssuedByfbca2013.p7c)

     * [P7Cs (Issued To)](http://http.fpki.gov/bridge/caCertsIssuedTofbca2013.p7c)

* ***SHA-1 Federal Root Certification Authority (SHA1 FRCA)***

     * [SHA1 FRCA CRL](http://http.fpki.gov/sha1frca/sha1frca.cr)

     * [P7Cs (Issued By)](http://http.fpki.gov/sha1frca/caCertsIssuedBysha1frca.p7c)

     * [P7Cs (Issued To)](http://http.fpki.gov/sha1frca/caCertsIssuedTosha1frca.p7c)

* ***Legacy Federal Common Policy Certification Authority (Legacy FCPCA)***

     * [Legacy FCPCA CRL](http://fpkia.gsa.gov/CommonPolicy/CommonPolicy%281%29.crl)

### Federal PKI Certificate Polices and Profiles ###

* ***Federal PKI Certificate Policies***

     * [Current Common CA and Bridge CA Certificate Policies](https://www.idmanagement.gov/IDM/s/article_content_old?tag=a0Gt0000000SfwS) 

- ***Federal PKI Certificate Profiles***

     * [FPKI X.509 Certificate and CRL Extensions Profile](https://www.idmanagement.gov/IDM/s/document_detail?Id=kA0t00000008Od8CAE)

     * [X.509 Certificate and Certificate Revocation List (CRL) Extensions Profile for PIV-I Cards](https://www.idmanagement.gov/IDM/s/document_detail?Id=kA0t00000008ObiCAE)

     * [X.509 Certificate and CRL Extensions Profile for the Shared Service Provider (SSP) Program](https://www.idmanagement.gov/IDM/s/document_detail?Id=kA0t0000000GmdcCAC)










