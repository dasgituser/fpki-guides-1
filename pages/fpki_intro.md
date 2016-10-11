---
layout: default
title: Introduction
permalink: /intro/
---
Welcome to the **Federal Public Key Infrastructure** (FPKI) guides!  

On these pages you will find information explaining what the Federal Public Key Infrastructure is, links to tools, links to Certificate Authorities, and tips to help you work with the certificates.  

These guides are [open source](https://github.com/gsa/fpki-guides) and a _work in progress_ and we [welcome contributions]({{ site.baseurl }}/contribute/) from our colleagues.

The information on this page provides introductory information.

1. [What is the Federal PKI?](#what-is-the-federal-pki)
2. [What is a Certificate?](#what-are-certificates) 
3. [What is a Certificate Policy?](#what-is-a-certificate-policy)
4. [What is a Certificate Authority?](#what-is-a-certificate-authority)
5. [What are Certificate Revocation Lists (CRLs)?](#what-are-certificate-revocation-lists)

### What is the Federal PKI? ###


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
