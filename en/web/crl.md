{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CRL File - Certificate Revocation List",
  "description":"Learn about CRL file format and APIs that can create and open CRL files.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2022-09-01"
}

## What is a CRL file?

A CRL (Certificate Revocation List) file is a blacklist of X.509 digital certificates that a certificate authority (CA) revokes prior to their assigned revocation date. It contains information about the issue and the revocation date that lets the security administrators to block affected digital certificates. CRL doesn't include expired certificates as its main purpose is to notify about the untrusted and invalid certificates.

Applications that can **open CRL files** include OpenSSL, Microsoft IIS Server, and Citrix NetScaler.

## CRL File Format - More Information

CRL files contain information in the X.509 standard which also defines its semantics for sharing public key information. Other information contained inside a CRL file may include the time limit for which the certificates have been revoked, reason for the revocation, serial number of revoked certificate and timestamp.


### Top Reasons for Certificates Getting Added to CRL

There could be  several reasons for getting your website's certificate revoked and being added to CRL. Some of them could be;

1. Your certificate's private key has been compromised
1. Your certificate is not valid or mis-issued by the CA
1. Organizational details associated with the certificate are changed and CA issues new certificate
1. Any other unavoidable reason for which the certificate has been revoked

## References

* [National Institute of Standards and Technology (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force’s (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Certification Revocation List](https://en.wikipedia.org/wiki/Certificate_revocation_list)
