---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---


Additional material of for the PAM 2023 submission *DissecTLS: A Scalable Active Scanner for TLS Server Configurations, Capabilities, and TLS Fingerprinting*.


## Abstract

Collecting metadata from TLS servers on a large scale allows to draw conclusions about their capabilities and configuration. Not only provides this new insights into the Internet but it enables use cases like detecting malicious C&C servers. However, active scanners can only observe and interpret the behavior of TLS servers, the underlying configuration and implementation causing the behavior remains hidden.
Existing approaches struggle between resource intensive scans that can reconstruct this data and light-weight fingerprinting approaches that aim to differentiate servers without making any assumptions about their inner working. With this work we propose DissecTLS, an active TLS scanner that is both light-weight enough to be used for Internet measurements and able to reconstruct the configuration and capabilities of the TLS stack. This was achieved by modeling the parameters of the TLS stack and derive an active scan that dynamically creates scanning probes based on the model and the previous responses from the server.
We provide a comparison of five active TLS scanner and fingerprinting approaches in a local testbed and on toplist targets. We conducted a measurement study over 9 weeks to fingerprint C&C servers and to analyze popular and deprecated TLS parameter usage. Similar to related work we achieved a 99% precision to detect C&C servers but could improve the recall by a factor of 2.8.

## Experiment Setup and Scanner Software

For the DissecTLS paper we have used a fork of the [TUM Goscanner](https://github.com/tumi8/goscanner) for our Internet measurements. We extended it with custom DissecTLS and JARM scan and open-sourced the code under [tba].

The experiment setup used ot compare the TLS scanner and fingerprinting tools can be found under: [experiment-setup](https://github.com/pam2023-51-dissectls/experiment-setup)

## Data

We provide an additional [ranking]({{ site.baseurl }}{% link pages/ranking.md %}) of TLS patameters extending the ones frome the paper.

## Reproducibility

tbd