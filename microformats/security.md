
# Security Microformat

[`security.txt`](https://securitytxt.org/) is <q cite="https://securitytxt.org/">a proposed standard which allows websites to define security policies.</q> As I raised in [issue #223](https://github.com/securitytxt/security-txt/issues/223), I don’t think plaintext is a very appropriate format to serve humans. An obvious solution would be for the standard to allow authors to serve the security file as <abbr>HTML</abbr>. However, we could then no longer rely on just text content for formatting, so I propose redefining `security.txt` as a [microformat](https://nl.wikipedia.org/wiki/Microformat), which uses the <q>humans first, machines second</q> principle.

## Profile

A ``security.txt`` meta data profile, using the [<abbr>XHTML</abbr> Meta Data Profiles](https://gmpg.org/xmdp/) microformat.

<dl class="profile">
    <dt id="class">class</dt>
    <dd>
        <dl>
            <dt id="security-expires">security-expires</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-expires">The "Expires" field indicates the date and time after which the data contained in the "security.txt" file is considered stale and should not be used (as per [Section 5.3](https://www.rfc-editor.org/rfc/rfc9116#stale)).</q>
            </dd>
            <dt id="security-preferred-languages">security-preferred-languages</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-preferred-languages">The "Preferred-Languages" field can be used to indicate a set of natural languages that are preferred when submitting security reports. This set **MAY** list multiple values, separated by commas. If this field is included, then at least one value **MUST** be listed.</q>
            </dd>
        </dl>
    </dd>
    <dt id="rel">rel</dt>
    <dd>
        <dl>
            <dt id="security-contact">security-contact</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-contact">The "Contact" field indicates a method that researchers should use for reporting security vulnerabilities such as an email address, a phone number, and/or a web page with contact information.</q>
            </dd>
            <dt id="security-encryption">security-encryption</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-encryption">The "Encryption" field indicates an encryption key that security researchers should use for encrypted communication.</q>
            </dd>
            <dt id="security-acknowledgments">security-acknowledgments</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-acknowledgments">The "Acknowledgments" field indicates a link to a page where security researchers are recognized for their reports. The page being referenced should list security researchers that reported security vulnerabilities and collaborated to remediate them. Organizations should be careful to limit the vulnerability information being published in order to prevent future attacks.</q>
            </dd>
            <dt id="security-canonical">security-canonical[^1]</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-canonical">The "Canonical" field indicates the canonical URIs where the "security.txt" file is located, which is usually something like "https://example.com/.well-known/security.txt".</q>
            </dd>
            <dt id="security-policy">security-policy</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-policy">The "Policy" field indicates a link to where the vulnerability disclosure policy is located. This can help security researchers understand the organization's vulnerability reporting practices.</q>
            </dd>
            <dt id="security-hiring">security-hiring</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-hiring">The "Hiring" field is used for linking to the vendor's security-related job positions.</q>
            </dd>
            <dt id="security-csaf">security-csaf</dt>
            <dd>
                <q cite="https://docs.oasis-open.org/csaf/csaf/v2.0/os/csaf-v2.0-os.html#abstract">The Common Security Advisory Framework (<abbr>CSAF</abbr>) Version 2.0 is the definitive reference for the language which supports creation, update, and interoperable exchange of security advisories as structured information on products, vulnerabilities and the status of impact and remediation among interested parties.</q>
                <q cite="https://docs.oasis-open.org/csaf/csaf/v2.0/os/csaf-v2.0-os.html#718-requirement-8-securitytxt">In the security.txt there MUST be at least one field <code>CSAF</code> which points to the <code>provider-metadata.json</code> (requirement 7).</q>
            </dd>
        </dl>
    </dd>
</dl>

### Source

```html
<dl class="profile">
    <dt id="class">class</dt>
    <dd>
        <dl>
            <dt id="security-expires">security-expires</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-expires">The "Expires" field indicates the date and time after which the data contained in the "security.txt" file is considered stale and should not be used (as per [Section 5.3](https://www.rfc-editor.org/rfc/rfc9116#stale)).</q>
            </dd>
            <dt id="security-preferred-languages">security-preferred-languages</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-preferred-languages">The "Preferred-Languages" field can be used to indicate a set of natural languages that are preferred when submitting security reports. This set **MAY** list multiple values, separated by commas. If this field is included, then at least one value **MUST** be listed.</q>
            </dd>
        </dl>
    </dd>
    <dt id="rel">rel</dt>
    <dd>
        <dl>
            <dt id="security-contact">security-contact</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-contact">The "Contact" field indicates a method that researchers should use for reporting security vulnerabilities such as an email address, a phone number, and/or a web page with contact information.</q>
            </dd>
            <dt id="security-encryption">security-encryption</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-encryption">The "Encryption" field indicates an encryption key that security researchers should use for encrypted communication.</q>
            </dd>
            <dt id="security-acknowledgments">security-acknowledgments</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-acknowledgments">The "Acknowledgments" field indicates a link to a page where security researchers are recognized for their reports. The page being referenced should list security researchers that reported security vulnerabilities and collaborated to remediate them. Organizations should be careful to limit the vulnerability information being published in order to prevent future attacks.</q>
            </dd>
            <dt id="security-canonical">security-canonical[^1]</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-canonical">The "Canonical" field indicates the canonical URIs where the "security.txt" file is located, which is usually something like "https://example.com/.well-known/security.txt".</q>
            </dd>
            <dt id="security-policy">security-policy</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-policy">The "Policy" field indicates a link to where the vulnerability disclosure policy is located. This can help security researchers understand the organization's vulnerability reporting practices.</q>
            </dd>
            <dt id="security-hiring">security-hiring</dt>
            <dd>
                <q cite="https://www.rfc-editor.org/rfc/rfc9116#name-hiring">The "Hiring" field is used for linking to the vendor's security-related job positions.</q>
            </dd>
            <dt id="security-csaf">security-csaf</dt>
            <dd>
                <q cite="https://docs.oasis-open.org/csaf/csaf/v2.0/os/csaf-v2.0-os.html#abstract">The Common Security Advisory Framework (<abbr>CSAF</abbr>) Version 2.0 is the definitive reference for the language which supports creation, update, and interoperable exchange of security advisories as structured information on products, vulnerabilities and the status of impact and remediation among interested parties.</q>
                <q cite="https://docs.oasis-open.org/csaf/csaf/v2.0/os/csaf-v2.0-os.html#718-requirement-8-securitytxt">In the security.txt there MUST be at least one field <code>CSAF</code> which points to the <code>provider-metadata.json</code> (requirement 7).</q>
            </dd>
        </dl>
    </dd>
</dl>
```
[^1]: Arguably, [`rel=canonical`](https://html.spec.whatwg.org/multipage/links.html#link-type-canonical) would be sufficient, and [`rel=security-canonical`](#security-canonical) is not needed.

## Example

```html
<dl class="security-txt">
    <dt>Contact</dt>
    <dd>
        <a rel="security-contact" href="mailto:security@example.com?subject=security.txt">security@example.com</a>
    </dd>
    <dt>Expires</dt>
    <dd>
        <time class="security-expires" datetime="2024-08-06T10:40:00.000Z">August 2024</time>
    </dd>
    <dt>Encryption</dt>
    <dd>
        <a rel="security-encryption" href="https://example.com/.well-known/pgp-key.txt"><abbr>PGP</abbr> key</a>
    </dd>
    <dt>Acknowledgments</dt>
    <dd>
        <a rel="security-acknowledgments" href="https://example.com/security/acknowledgments">https://example.com/security/acknowledgments</a>
    </dd>
    <dt>Preferred-Languages</dt>
    <dd class="security-preferred-languages"><abbr title="English">en</abbr>, <abbr title="Dutch">nl</abbr></dd>
    <dt>Canonical[^1]</dt>
    <dd><a rel="security-canonical" href="https://example.com/.well-known/security">https://example.com/.well-known/security</a></dd>
    <dt>Policy</dt>
    <dd><a rel="security-policy" href="https://example.com/security/policy">https://example.com/security/policy</a></dd>
    <dt>Hiring</dt>
    <dd><a rel="security-hiring" href="https://example.com/security/jobs">https://example.com/security/jobs</a></dd>
    <dt>CSAF</dt>
    <dd><a rel="security-csaf" href="https://example.com/.well-known/csaf/provider-metadata.json">https://example.com/.well-known/csaf/provider-metadata.json</a></dd>
</dl>
```

This example was based on the following ``security.txt`` sample:

```text
Contact: mailto:security@example.com
Expires: 2024-08-06T10:40:00.000Z
Encryption: https://example.com/pgp-key.txt
Acknowledgments: https://example.com/security/acknowledgments
Preferred-Languages: en, nl
Canonical: https://example.com/.well-known/security
Policy: https://example.com/security/policy
Hiring: https://example.com/security/jobs
CSAF: https://example.com/.well-known/csaf/provider-metadata.json
```
