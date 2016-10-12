---
layout: default
title: CRLs And Certificates
permalink: /crls/
---
<div style="float:right; padding:10px; margin-right:20px; border-radius:10px; width:180px; height:40px; box-shadow:3px 3px 5px 0px; text-align:center; background-color:#CCC; color:#666666">
<div style="color:#000000">
<em>Advanced</em>
</div>
</div>

This section will provide you with a brief overview of Certificate Revocation Lists (CRLs) and downloadable links to the commonly requested Federal PKI artifacts.

### Certificate Revocation Lists ###
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

### ***Illustration of a Certificate and CRL***

<img src="/img/crls_diagram1.jpg"/>

### Federal Common Policy Certification Authority (Common or FCPCA) ###
*Note: To request a secure distribution of the Common CA Root Certificate, please contact the [FPKIMA](mailto:fpki-help@gsa.gov)*

* Common CA Root Certificate:   [http://http.fpki.gov/fcpca/fcpca.crt](http://http.fpki.gov/fcpca/fcpca.crt)

* The DN for the Common Policy CA is:  **cn=Federal Common Policy CA, ou=FPKI, o=U.S. Government, c=US** 

* The sha1 Thumbprint is:   **90 5f 94 2f d9 f2 8f 67 9b 37 81 80 fd 4f 84 63 47 f6 45 c1**

* P7Cs (Issued By):  [http://http.fpki.gov/fcpca/caCertsIssuedByfcpca.p7c](http://http.fpki.gov/fcpca/caCertsIssuedByfcpca.p7c)

* P7Cs (Issued To):  [http://http.fpki.gov/fcpca/caCertsIssuedTofcpca.p7c](http://http.fpki.gov/fcpca/caCertsIssuedTofcpca.p7c)

* FCPCA CRL: [http://http.fpki.gov/fcpca/fcpca.cr](http://http.fpki.gov/fcpca/fcpca.cr) 

### Federal Bridge Certificate Authority (Bridge or FBCA) ###

* P7Cs (Issued By): [http://http.fpki.gov/bridge/caCertsIssuedByfbca2013.p7c](http://http.fpki.gov/bridge/caCertsIssuedByfbca2013.p7c)

* P7Cs (Issued To): [http://http.fpki.gov/bridge/caCertsIssuedTofbca2013.p7c](http://http.fpki.gov/bridge/caCertsIssuedTofbca2013.p7c)

* FBCA CRL: [http://http.fpki.gov/bridge/fbca.crl](http://http.fpki.gov/bridge/fbca.crl)

* FBCA 2013 CRL: [http://http.fpki.gov/bridge/fbca2013.c](http://http.fpki.gov/bridge/fbca2013.crl)

### SHA-1 Federal Root Certificate Authority (SHA1 FRCA) ###

* P7Cs (Issued By): [http://http.fpki.gov/sha1frca/caCertsIssuedBysha1frca.p7c](http://http.fpki.gov/sha1frca/caCertsIssuedBysha1frca.p7c)

* P7Cs (Issued To): [http://http.fpki.gov/sha1frca/caCertsIssuedTosha1frca.p7c](http://http.fpki.gov/sha1frca/caCertsIssuedTosha1frca.p7c)

* SHA1 FRCA CRL: [http://http.fpki.gov/sha1frca/sha1frca.cr](http://http.fpki.gov/sha1frca/sha1frca.cr)

### Legacy Federal Common Policy Certificate Authority (Legacy FCPCA) ###

* Legacy FCPCA CRL: [http://fpkia.gsa.gov/CommonPolicy/CommonPolicy(1).crl](http://fpkia.gsa.gov/CommonPolicy/CommonPolicy%281%29.crl)
