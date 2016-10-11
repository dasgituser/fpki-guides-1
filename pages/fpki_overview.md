---
layout: default
title: Federal PKI Overview
permalink: /overview/
---
<div style="float:right; padding:10px; margin-right:20px; border-radius:10px; width:180px; height:40px; box-shadow:3px 3px 5px 0px; text-align:center; background-color:#CCC; color:#666666">
<div style="color:#000000">
<em>Introduction</em>
</div>
</div>
## Overview

The Federal Public Key Infrastructure encompasses the Certificate Authorities which issue:

1. PIV credentials and person identity certificates 
2. PIV-Interoperable credentials and person identity certificates
3. Other person identity certificates
4. Device identity certificates

The participating Certificate Authorities **and** the Policies, Processes, and Auditing of all the participants is referred to as the **Federal Public Key Infrastructure (FPKI)**

## Example
To give a simple example, we'll explain the PIV certificates.  Although we have many other types of identity certificates, it's easiest to explain with **PIV** since you might have one: 

* Identity certificates are issued and digitally signed by a _Certificate Authority_.  
* The _Certificate Authority_ that issued and digitally signed your PIV certificates is called an _Intermediate Certificate Authority_ because it was issued a certificate by another _Certificate Authority_.  
* This process of issuing and signing continues until there is one  _Certificate Authority_ that is called the _Root Certificate Authority_.

The full process of proving identity when issuing the certificates, auditing the certificate authorities, and the cryptographic protections of the digital signatures establish the basis of Trust. 

![Example of an identity certificate with intermediate and root](../img/certificatechain_small.png){:style="float:center"}

The US Federal Government has also established Trust with other Certificate Authorities which serve business communities, State and Local government communities, and international government communities.

For the US Federal Government Executive branch agencies, there is one Root Certificate Authority named _Federal Common Policy Certificate Authority (COMMON)_, and dozens of Intermediate Certificate Authorities, and Bridged Certificate Authorities.  

*  [A graph of the federal public key infrastructure, including the business communities](https://fpki-graph.fpki-lab.gov/)

<!-- TODO: Reuse same information and visuals from here https://github.com/GSA/piv-guides/blob/staging/pages/certchains.md -->

### What is a Certificate? ###

![Example of certificate fields](https://raw.githubusercontent.com/djpackham/fpki-guides/gh-pages/img/certFieldsEx.png){:style="float:right"}

Certificates are files that can be used for gaining access to networks, applications, digitally signing, encrypting, or creating trusted connections. You can review [Details of a PIV Credential](https://gsa.github.io/piv-guides/details/) to learn more about viewing, exporting and understanding PIV certificates. You can also review the [HTTPS-Only Standard](https://https.cio.gov/certificates/) to learn more about certificates use in HTTPS connections.

A certificate can be issued to a person or a device. A certificate includes information about the person/device, the issuer of the certificate, the purpose(s) of the certificate, and other information to verify if the certificate is valid. An example of the common fields/values you'd find in a certificate can be seen to the right.

Similar to a paper certificate, certificates are made valid when they are signed by a recognized and trustworthy authority, known as a Certificate Authority (CA). Learn more about Certificate Authorities by reviewing the [Certificate Authorities page](/ca/). Also, learn more about the different types of certificates by reviewing the [What are the Different Types of Certificates and their Purpose page](/pki/).

### What is a Certificate Policy? ###

All certificates are not used for the same reason or issued by the same Certificate Authority. Some certificates may be used for digitally signing a document, another certificate may be used for logging into a website. In simple terms, we can say that a certificate policy is a set of rules used to define the use of a certificate.

Similar to other PKIs, the Federal PKI has defined their own set of rules, or certificate policies, for Federal certificates. In-depth details on the certificate profiles are contained in the current and historical Federal Public Key Infrastructure (FPKI) Policy documents. This table contains links to the most recent documents:

| Certificates    | Policy Update Date  | Link to Profile Information|
| -------------            |:----:               |:----:|
| PIV Certificates           | May 5, 2015             | [Worksheets 5, 6, 8 and 9 in this document](https://www.idmanagement.gov/IDM/servlet/fileField?entityId=ka0t0000000TNP2AAO&field=File__Body__s)|

### What is a Certificate Authority? ###

### What are Certificate Revocation Lists (CRLs)? ###
