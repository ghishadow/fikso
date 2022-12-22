# about:config settings

## QOL

- set dom.webgpu.enabled to true for WebGPU

## Disable Pocket

``` text
extensions.pocket.enabled = false
```

## TLS hardening

``` text
// Disable weak ciphersuites
security.ssl3.ecdhe_ecdsa_aes_128_sha = false
security.ssl3.ecdhe_ecdsa_aes_256_sha = false
security.ssl3.dhe_rsa_aes_128_sha = false
security.ssl3.dhe_rsa_aes_256_sha = false
security.ssl3.ecdhe_rsa_aes_128_sha = false
security.ssl3.ecdhe_rsa_aes_256_sha = false
security.ssl3.rsa_aes_128_gcm_sha256 = false
security.ssl3.rsa_aes_128_sha = false
security.ssl3.rsa_aes_256_gcm_sha384 = false
security.ssl3.rsa_aes_256_sha = false
security.ssl3.rsa_des_ede3_sha = false
security.ssl.enable_false_start  = false

security.ssl.require_safe_negotiation = true


// Enable Encrypted Client Hello (ECH/ESNI)
network.dns.echconfig.enabled = true
network.dns.http3_echconfig.enabled = true
network.dns.use_https_rr_as_altsvc = true

// Enable OCSP checks
security.OCSP.require = true

// Enforce CRLite revocation checks
security.pki.crlite_mode = 2


```

## Privacy

``` text

// Use DoH without fallback to insecure DNS
network.trr.mode = 3

// Reject all Third-Party cookies
network.cookie.cookieBehavior = 1

// Disable Referer header
network.http.sendRefererHeader = 0

// Send DoNotTrack
privacy.donottrackheader.enabled = true

// Configure Tracking Protection
privacy.trackingprotection.enabled = true
privacy.trackingprotection.emailtracking.enabled = true
privacy.trackingprotection.lower_network_priority = true
privacy.trackingprotection.fingerprinting.enabled = true
privacy.trackingprotection.cryptomining.enabled = true
privacy.trackingprotection.socialtracking.enabled = true
privacy.socialtracking.block_cookies.enabled = true
privacy.trackingprotection.origin_telemetry.enabled = true

privacy.userContext.enabled = true
privacy.userContext.ui.enabled = true

// Enable First-Party Isolation
// TODO: experiment with privacy.firstparty.isolate.use_site and privacy.firstparty.isolate.block_post_message
privacy.firstparty.isolate = true

// Resist browser fingerprinting
privacy.resistFingerprinting = true
privacy.spoof_english = 2

// Disable pre-fetching
network.dns.disablePrefetch = true
network.prefetch-next = false

// Remove tracking identifiers from urls
privacy.query_stripping.enabled = true
```

## Hardware Video Acceleration

## Performance Settings

``` text

// set according to your pc
dom.ipc.processCount = 4

browser.preferences.defaultPerformanceSettings.enabled = false

```

Disable CSS backdrop

```
layout.css.backdrop-filter.enabled
```

### References

- <https://wiki.archlinux.org/title/Firefox/Tweaks>
- <https://wiki.gentoo.org/wiki/Firefox>


## Sound and Video
Disable VP9 and use AV1 in Linux/Windows, HEVC in MacOS


