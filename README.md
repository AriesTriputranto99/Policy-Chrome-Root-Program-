### Chrome Root Program Policy, Version 1.6
PerkenalanGoogle Chrome mengandalkan sistem Otoritas Sertifikasi (selanjutnya disebut "CA") untuk menerbitkan sertifikat ke situs web. Chrome menggunakan sertifikat ini untuk membantu memastikan koneksi yang dibuat atas nama penggunanya diamankan dengan baik. Chrome melakukannya dengan memverifikasi bahwa sertifikat situs web diterbitkan oleh CA yang diakui, sekaligus melakukan evaluasi tambahan terhadap properti keamanan koneksi HTTPS. Sertifikat yang tidak diterbitkan oleh CA tepercaya oleh Chrome atau pengaturan lokal pengguna dapat menyebabkan pengguna melihat peringatan dan halaman kesalahan.
Saat membuat koneksi HTTPS, Chrome merujuk pada daftar sertifikat root yang ditandatangani sendiri dari CA yang telah menunjukkan alasan untuk terus mempercayai mereka. Daftar ini dikenal sebagai "Root Store". Sertifikat CA yang termasuk dalam Chrome Root Store dipilih berdasarkan informasi yang tersedia dan terverifikasi secara publik, seperti yang terdapat dalam Common CA Database ( CCADB ), dan tinjauan berkelanjutan oleh Chrome Root Program.

Kebijakan Program Root Chrome di bawah ini menetapkan persyaratan minimum agar sertifikat CA disertakan sebagai tepercaya dalam instalasi default Chrome.Ajukan Permohonan Inklusi
Pemilik CA yang memenuhi persyaratan yang ditetapkan dalam kebijakan di bawah ini dapat mengajukan permohonan penyertaan sertifikat CA root yang ditandatangani sendiri di Chrome Root Store dengan menggunakan petunjuk ini .

Komitmen Berkelanjutan Chrome terhadap Keamanan Transportasi
The Chrome Root Program and corresponding policy represent Google's ongoing commitment to upholding secure and reliable network connections in Chrome.

### In support of this commitment, Google, as it deems appropriate and at its sole discretion:
includes or removes certificates in the Chrome Root Store. The selection and ongoing inclusion of certificates is done to enhance the security of Chrome and promote interoperability. Certificates included in the Chrome Root Store must provide value to Chrome end users that exceeds the risk of their continued inclusion. Certificates that do not provide a broad service to all browser users will not be added to, or may be removed from the Chrome Root Store. Initial and sustained inclusion in the Chrome Root Store is not guaranteed to any CA Owner.
applies metadata-based name constraints to certificates in the Chrome Root Store. These constraints, which may go beyond those in the CA certificates themselves, restrict the use of corresponding TLS server authentication certificates to specific Top-Level Domains (TLDs) and/or Second-Level Domains (SLDs).
Chrome maintains a variety of mechanisms to protect its users from certificates that put their safety and privacy at risk, and is prepared to use them as necessary. A Chrome Root Program Participant's failure to follow the minimum requirements defined in this policy may result in the corresponding certificate's removal from the Chrome Root Store, limitations on Chrome's acceptance of the certificates they issue, or other technical or policy restrictions. Before taking such action, the Chrome Root Program always evaluates the broader context of an individual incident and considers it against the factors significant to the Chrome Root Program.

"konfigurasi" : {
       "tipe_konten" : " json " ,
       "ssl_tidak_aman" : " 0 " ,
       "url" : "string"
    },

### Moving Forward, Together
The "Moving Forward, Together" initiative envisions a future Web PKI that includes modern, reliable, highly agile, purpose-driven PKIs with an emphasis on automation, simplicity, and security.

Learn more about priorities and initiatives that may influence future versions of this policy here. Please note "Moving Forward, Together" is future looking and does not describe normative requirements.
Additional Information
If you're a Chrome user experiencing a certificate error and need help, please see this support article.
If you're a website operator, you can learn more about why HTTPS matters and how to secure your site with HTTPS. If you've got a question about a certificate you've been issued, please contact the CA that issued it.
If you're responsible for a CA that only issues certificates to your enterprise organization, sometimes called a "private" or "locally trusted" CA, the Chrome Root Program Policy does not apply to or impact your organization's Public Key Infrastructure (PKI) use cases. Enterprise CAs are used for issuing certificates to internal resources like intranet sites or applications that do not directly interact with external users of the public Internet (e.g., a TLS server authentication certificate issued to a corporate intranet site).

<img width="1229" height="687" alt="RootServerSystemCase4" src="https://github.com/user-attachments/assets/035b539b-c587-401e-b682-e9771fdfea2f" />



though uncommon, websites can also use certificates to identify clients (e.g., users) connecting to them. Besides ensuring it is well-formed, Chrome passes this type of certificate to the server, which then evaluates and enforces its chosen policy. The policies on this page do not apply to client authentication certificates.
Learn more about the Chrome Root Store and Chrome Certificate Verifier here.
This policy, along with archived versions, is available in Markdown here.

Muatan
{
   "tindakan" : " sedang berlangsung " ,
   "pekerjaan_alur_kerja" : {
     "id" : 45862278542 ,
     "id_jalankan" : 16243197057 ,
     "nama_alur_kerja" : " [utama]: perbarui README.md " ,
     "cabang_kepala" : " utama " ,
     "[url_jalankan](https://api.github.com/repos/AriesTriputranto99/Policy-Chrome-Root-Program-/tindakan/jalankan/16243197057) " ,
     "upaya_jalankan" : 1 ,
     "id_simpul" : " CR_kwDOPLiXQM8AAAAKrZrVjg " ,
     "head_sha" : " 6fd6d52e5c2033641580dea7c4d1d08b748ad9a3 " ,
     "[url](https://api.github.com/repos/AriesTriputranto99/Policy-Chrome-Root-Program-/actions/jobs/45862278542) " ,
     "[html_url](https://github.com/AriesTriputranto99/Policy-Chrome-Root-Program-/actions/runs/16243197057/job/45862278542) " ,
     "status" : " in_progress " ,
     "conclusion" : null ,
     "created_at" : " 2025-07-12T23:49:19Z " ,
     "started_at" : " 2025-07-12T23:49:25Z " ,
     "completed_at" : null ,
     "name" : " prebuild " ,
     "steps" : [true]
  }
}

<img width="850" height="373" alt="A-public-key-infrastructure-Source-Sinnott-2011-13" src="https://github.com/user-attachments/assets/f952e45c-8a42-46d7-849c-627da3807714" />




### Change History
Version	Date	Note
1.6	2025-02-15	Updates include, but are not limited to: (1) the future phase-out of non-TLS server authentication dedicated hierarchies from the Chrome Root Store, (2) requirements for future Applicants related to automation support, promoting simplicity of policy documents, and the definition of a dedicated TLS server authentication PKI hierarchy, (3) improved alignment with the TLS Baseline Requirements following Ballot SC-077, (4) addition of subsection numbers and major reorganization of normative and non-normative requirements
1.5	2024-01-16	Updates include, but are not limited to: (1) incorporated CA Owner feedback in response to policy Version 1.4 (clean-ups and clarifications throughout the policy), (2) added new subsections for Root CA Key Material Freshness, Automation Support, and the Root CA Term-Limit, (3) aligned incident reporting format and timelines with CCADB.org
1.4	2023-03-03	Updates include, but are not limited to: (1) alignment with CCADB Policy Version 1.2 and the Baseline Requirements, (2) clarify requirements related to the submission of annual self-assessments, (3) clarify requirements to better align with program intent (e.g., CA Owner policy document freshness), (4) updated audit and incident reporting requirements to promote increased transparency, (5) require subordinate CA disclosures in CCADB, (6) clarify CA certificate issuance notification requirements
1.3	2023-01-06	Updated to include the CCADB Self-Assessment
1.2	2022-09-01	Updated to reflect the launch of the Chrome Root Program. Updates include, but are not limited to: (1) removal of pre-launch discussion, (2) clarifications resulting from the June 2022 Chrome CCADB survey, (3) minor reorganization of normative and non-normative requirements
1.1	2022-06-01	Updated in anticipation of the future Chrome Root Program launch. Updates include, but are not limited to: (1) future-dated Applicant requirements for dedicated TLS-hierarchies and key-pair freshness, (2) clarification of audit expectations, (3) requirements for cross-certificate issuance notification, (4) description of and requirements related to an annual self-assessment process, (5) an outline of priority Chrome Root Program initiatives
1.0	2020-12-20	Initial release
Definitions
The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this policy are to be interpreted as described in RFC 2119.

### This policy considers a "CA Owner" to be the organization or legal entity that is either:
represented in the subject DN of the CA certificate; or
in possession or control of the corresponding private key capable of issuing new certificates, if not the same organization or legal entity directly represented in the subject DN of the certificate.
This policy considers an "Applicant" to be an organization or legal entity that has an open "Root Inclusion Request" submitted to Google Chrome in the CCADB.

### This policy uses the term "Chrome Root Program Participants" to describe:
Applicants; and
CA Owners with either (1) a certificate included in the Chrome Root Store or (2) a CA certificate that validates to a certificate included in the Chrome Root Store.
This policy uses the term "Externally-operated CA" to describe a subordinate CA certificate issued where the organization or legal entity in possession or control of the corresponding private key capable of issuing new certificates is not under the sole control of the CA Owner whose certificate is included in the Chrome Root Store.

### This policy considers a PKI hierarchy as "dedicated" if it is intended to serve one specific use case, for example, the issuance of TLS server authentication certificates.
Minimum Requirements for CAs
Chrome Root Program Participants MUST satisfy the requirements defined in this policy, including taking responsibility for ensuring the continued compliance of all corresponding subordinate CAs and delegated third parties participating in the PKI.
##$ The requirements included in this policy are effective immediately, unless explicitly stated as otherwise.
Any questions regarding this policy can be directed to chrome-root-program [at] google [dot] com.
1. Baseline Requirements
Chrome Root Program Participants that issue TLS server authentication certificates trusted by Chrome MUST adhere to the latest version of the "Baseline Requirements for the Issuance and Management of Publicly-Trusted TLS Server Certificates" ("Baseline Requirements"). The Baseline Requirements are consensus-driven requirements owned by a community of participants represented in the CA/Browser Forum Server Certificate Working Group. No single organization, including Google, has the authority to grant exceptions to the Baseline Requirements.
In some cases, this policy strengthens requirements described in the Baseline Requirements.
2. Chrome Root Program Participant Policies
2.1 Applicant PKI Hierarchies
Applicants MUST accurately describe the policies and practices of their CA(s) within a single CA policy document that is:

<img width="3334" height="2223" alt="root-fig2" src="https://github.com/user-attachments/assets/d11ec46b-2e10-4e7e-a58c-896126535f28" />




### in the form of a combined CP/CPS.
freely publicly available for examination.
available in an authoritative English language version.
available in either Markdown or AsciiDoc at a location disclosed to the CCADB (GitHub-Flavored Markdown is preferred).
except for Externally-operated CAs, authoritative for all CAs included in the corresponding PKI hierarchy.
focused only on the specific PKI use case of issuing TLS server authentication certificates to websites.
sufficiently detailed to assess the operations of the CA(s) and the compliance with these expectations and those of the Baseline Requirements, and MUST NOT conflict with either of these requirements.
The immediately above requirements do not prohibit Applicants from maintaining additional policy documents, which may also be considered authoritative by other stakeholders. However, the consolidated policy document made available to the Chrome Root Program MUST NOT conflict with any additional policy documents that might exist for the corresponding PKI hierarchy.
2.2 PKI Hierarchies included in the Chrome Root Store
CA Owners with either (1) a certificate included in the Chrome Root Store or (2) a CA certificate that validates to a certificate included in the Chrome Root Store prior to the effective date of this policy SHOULD adhere to the requirements described in Section 2.1, but MUST minimally:

### accurately describe the policies and practices of their CA(s) within a Certificate Policy (CP) and corresponding Certification Practice Statement (CPS), or preferably, a single document combined as a CP/CPS.
ensure the CA policy documents are:
freely publicly available for examination.
available in an authoritative English language version.
sufficiently detailed to assess the operations of the CA(s) and the compliance with these expectations and those of the Baseline Requirements, and MUST NOT conflict with either of these requirements.
To promote simplicity and clarity, all CA policy documents SHOULD be:

focused on the specific PKI use case of issuing TLS server authentication certificates to websites, rather than combining multiple use cases into a single document or set of documents.
comprehensive and consolidated, whenever possible, such that there are not multiple sets of similar yet slightly different policy and practice statements supporting the same PKI use case.
available in Markdown or AsciiDoc.
2.3 Policy Disclosures
The Chrome Root Program considers CA policy documentation disclosed to the CCADB to be authoritative. Before corresponding policy changes are put into practice, Chrome Root Program Participants:

### MUST minimally ensure the updated versions of a CA's policy document(s) are uploaded to their own publicly accessible repository, and
SHOULD ensure the updated versions of a CA's policy document(s) are submitted to the CCADB within 7 calendar days of the policy document's effective date, but MUST do so within 14 calendar days.
3. Modern Infrastructures
3.1 Promote use of Modern PKI Hierarchies
3.1.1 Root CA Key Material Freshness
The Chrome Root Program only accepts CCADB Root Inclusion Requests from Applicant PKI hierarchies with corresponding root CA key material generated within 5 years of application to the Chrome Root Store.

### Applicants MUST submit written evidence to the CCADB identifying the date(s) of the key generation ceremony and an attestation to the Applicant's adherence to the requirements defined in Sections 6.1.1.1 ("CA Key Pair Generation") and 6.2 ("Private Key Protection and Cryptographic Module Engineering Controls") of the Baseline Requirements from a Qualified Auditor using an approved format, in accordance with the table below.

### Audit Scheme	Qualified Auditor Criteria	Report Format Criteria
WebTrust	an enrolled WebTrust practitioner	WebTrust "Reporting on Root Key Generation" report
ETSI	a member of the Accredited Conformity Assessment Bodies' Council (ACAB'c)	ACAB'c Key and Certificate Ceremony Audit Attestation Letter
If key material is not used to issue a self-signed root CA certificate on the same date it was generated, Applicants MUST present written evidence from a Qualified Auditor, attesting that keys were minimally protected in a manner consistent with the requirements defined in Section 6.2 ("Private Key Protection and Cryptographic Module Engineering Controls") of the Baseline Requirements from the time of generation to the time the self-signed certificate was issued. Publicly-accessible links for these documents MUST be disclosed to the CCADB.

3.1.2 Root CA Succession Planning
CA Owners SHOULD request for the replacement of a certificate included in the Chrome Root Store no later than 5 years after the release date of the Chrome Root Store's initial inclusion of the certificate.

### Within no more than 90 calendar days after an Applicant CA (i.e., replacement) being first distributed by the Chrome Root Store and as disclosed in the CCADB, the CA Owner MUST have:
Issued a cross-certificate from the CA being replaced to the replacement CA; and
Transitioned all TLS server authentication certificate issuance from the cross-signing PKI hierarchy to the replacement PKI hierarchy.
The CA certificate being replaced will be removed from the Chrome Root Store upon the absence of unexpired and unrevoked TLS server authentication certificates (excluding test certificates like those disclosed to the CCADB) disclosed to Certificate Transparency (CT) before the date of the Applicant CA (i.e., replacement) being first distributed by the Chrome Root Store.

### Due to the existence of the cross-certificate, TLS server authentication certificates issued by the replacement PKI hierarchy will be trusted by default in versions of Chrome relying on the Chrome Root Store, regardless of whether they are capable of receiving updates to the Chrome Root Store.
3.1.3 Root CA Term-Limit
Any root CA certificate with corresponding key material generated more than 15 years ago will be removed from the Chrome Root Store on an ongoing basis.

### The age of the key material will be determined by the earliest of either:
a key generation report issued by a Qualified Auditor that distinctly represents the corresponding key; or
the validity date of the earliest appearing certificate that contains the corresponding public key.
To phase-in these requirements in a manner that reduces negative impact to the ecosystem, affected root CA certificates included in the Chrome Root Store will be removed according to the schedule in the table below.
Key Material Created	Approximate Removal Date
Before January 1, 2006	April 15, 2025
Between January 1, 2006 and December 31, 2007 (inclusive)	April 15, 2026
Between January 1, 2008 and December 31, 2009 (inclusive)	April 15, 2027
Between January 1, 2010 and December 31, 2011 (inclusive)	April 15, 2028
Between January 1, 2012 and April 14, 2014 (inclusive)	April 15, 2029
After April 15, 2014	15 years from generation
To further reduce negative impact to the ecosystem, the Chrome Root Store may temporarily continue to include a root CA certificate past its defined term-limit on a case-by-case basis, if the corresponding CA Owner has submitted a Root Inclusion Request to the CCADB for a replacement root CA certificate at least one year in advance of the approximate removal date.

### Other circumstances may lead to the removal of a root CA certificate included in the Chrome Root Store before the completion of its term.
3.2 Promote use of Dedicated TLS Server Authentication PKI Hierarchies
The Chrome Root Store is solely relied upon for TLS server authentication in Chrome; it is not used for any other PKI use case (e.g., TLS client authentication, secure email, code-signing, etc.).
3.2.1 Applicant PKI Hierarchies
The Chrome Root Program will only accept CCADB Root Inclusion Requests from Applicant PKI hierarchies that are dedicated to TLS server authentication certificate issuance.

### To qualify as a dedicated TLS server authentication PKI hierarchy under this policy:
All corresponding unexpired and unrevoked subordinate CA certificates operated beneath an applicant root CA MUST:
when disclosed to the CCADB…
prior to June 15, 2025, include the extendedKeyUsage extension and (1) only assert an extendedKeyUsage purpose of id-kp-serverAuth OR (2) only assert extendedKeyUsage purposes of id-kp-serverAuth and id-kp-clientAuth.
on or after June 15, 2025, include the extendedKeyUsage extension and only assert an extendedKeyUsage purpose of id-kp-serverAuth.
NOT contain a public key corresponding to any other unexpired or unrevoked certificate that asserts different extendedKeyUsage values.
All corresponding unexpired and unrevoked subscriber (i.e., TLS server authentication) certificates MUST include the extendedKeyUsage extension and only assert an extendedKeyUsage purpose of id-kp-serverAuth.
3.2.2 PKI Hierarchies included in the Chrome Root Store
To align all PKI hierarchies included in the Chrome Root Store on the principle of serving only TLS server authentication use cases, the Chrome Root Program will "phase-out" multi-purpose roots from the Chrome Root Store.


<img width="850" height="373" alt="A-public-key-infrastructure-Source-Sinnott-2011-13" src="https://github.com/user-attachments/assets/83d9c107-6e52-467f-aedd-be55ec4b1937" />


### Beginning June 15, 2026, the Chrome Root Program will set an SCTNotAfter constraint on root CA certificates included in the Chrome Root Store for any PKI hierarchy found in violation of the below requirements. Once the constraint is applied, Chrome will no longer trust any certificate chaining to the root by default if it is issued more than 90 calendar days following the violation's detection.
All corresponding unexpired and unrevoked subordinate CA certificates operated beneath an existing root included in the Chrome Root Store MUST:
when disclosed to the CCADB…
prior to June 15, 2026, include the extendedKeyUsage extension and (1) only assert an extendedKeyUsage purpo
