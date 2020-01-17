---
layout: col-sidebar
title: ZAPping the OWASP Top 10
tags: zap
 ---

# ZAPping the OWASP Top 10

This document gives an overview of the automatic and manual components provided by the [OWASP Zed Attack Proxy Project (ZAP)](https://www.zaproxy.org) that are recommended for testing each of the OWASP Top Ten Project 2017 risks.

Note that the [OWASP Top Ten Project](https://www.owasp.org/index.php/OWASP_Top_Ten_Project) risks cover a wide range of underlying vulnerabilities, some of which are not really possible to test for in a completely automated way. If a completely automated tool claims to protect you against the full OWASP Top Ten then you can be sure they are being ‘economical with the truth’!

A printable (pdf) version of this document is also available (based on the Top 10 - 2013 edition): [ZAPpingTheOwaspTop10-2013.pdf](assets/ZAPpingTheOwaspTop10-2013.pdf).

The component links take you to the relevant places in an online version of the ZAP User Guide from which you can learn more. 

|                    | Common Components                                                                                                                                                              |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    | The 'common components' can be used for pretty much everything, so can be used to help detect all of the Top 10                                                                |
| Manual             | [Man-in-the-middle proxy](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsIntercept)                                                                            |
| Manual             | [Manual request](https://github.com/zaproxy/zap-core-help/wiki/HelpUiDialogsMan_req) / [resend](https://github.com/zaproxy/zap-core-help/wiki/HelpUiDialogsResend)             |
| Manual             | [Scripts](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsScriptsScripts)                                                                                              |
| Manual             | [Search](https://github.com/zaproxy/zap-core-help/wiki/HelpUiTabsSearch)                                                                                                       |
| **A1**             | [A1 Injection](https://www.owasp.org/index.php/Top_10-2017_A1-Injection)                                                                                                       |
| Automated          | [Active Scan Rules](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsAscan) ([Release](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsAscanrulesAscanrules), [Beta*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAscanrulesBetaAscanbeta), and [Alpha*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAscanrulesAlphaAscanalpha)) |
| Automated          | Advanced SQLInjection Scanner* (Based on SQLMap)                                                                                                                                                |
| Manual             | [Fuzzer](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsFuzz), combined with the [FuzzDb*](https://github.com/zaproxy/zap-extensions/wiki/AddOn_fuzzdb) and SVN Digger* files |
| **A2**             | [A2 Broken Authentication](https://www.owasp.org/index.php/Top_10-2017_A2-Broken_Authentication)                                                                               |
| Manual             | [HTTP Sessions](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsHttpsessions)                                                                                   |
| Manual             | [Spider](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsSpider)                                                                                                |
| Manual             | [Forced Browse](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsBruteForceConcepts)                                                                             |
| Manual             | [Token Generator*](https://github.com/zaproxy/zap-extensions/wiki/AddOn_tokengen)                                                                                       |
| Automatic          | [Access Control Testing*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAccessControlConcepts)                                                                      |
| **A3**             | [A3 Sensitive Data Exposure](https://www.owasp.org/index.php/Top_10-2017_A3-Sensitive_Data_Exposure)                                                                           |
| Automated          | [Active Scan Rules](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsAscan) ([Release](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsAscanrulesAscanrules), [Beta*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAscanrulesBetaAscanbeta), and [Alpha*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAscanrulesAlphaAscanalpha)) |
| Automated          | [Passive Scan Rules](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsPscan) ([Release](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsPscanrulesPscanrules), [Beta*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsPscanrulesBetaPscanbeta), and [Alpha*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsPscanrulesAlphaPscanalpha)) |
| **A4**             | [A4 XML External Entities (XXE)](https://www.owasp.org/index.php/Top_10-2017_A4-XML_External_Entities_(XXE))                                                                   |
| Automatic          | [Active Scan Rules](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsAscan) ([Release](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsAscanrulesAscanrules), [Beta*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAscanrulesBetaAscanbeta), and [Alpha*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAscanrulesAlphaAscanalpha)) |
| **A5**             | [A5 Broken Access Control](https://www.owasp.org/index.php/Top_10-2017_A5-Broken_Access_Control)                                                                               |
| Automated          | [Active Scan Rules](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsAscan) ([Release](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsAscanrulesAscanrules), [Beta*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAscanrulesBetaAscanbeta), and [Alpha*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAscanrulesAlphaAscanalpha)) |
| Automated          | [Passive Scan Rules](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsPscan) ([Release](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsPscanrulesPscanrules), [Beta*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsPscanrulesBetaPscanbeta), and [Alpha*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsPscanrulesAlphaPscanalpha)) |
| Automated          | [Access Control Testing*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAccessControlConcepts)                                                                      |
| Manual             | [HttpsInfo*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsHttpsinfoHttpsinfo)                                                                              |
| Manual             | [Port Scanner*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsPortscanConcepts)                                                                              |
| Manual             | [Wappalyzer - Technology detection*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsWappalyzerWappalyzer)                                                    |
| **A6**             | [A6 Security Misconfiguration](https://www.owasp.org/index.php/Top_10-2017_A6-Security_Misconfiguration)                                                                       |
| Manual             | [Spider](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsSpider)                                                                                                |
| Manual             | [Ajax Spider](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsSpiderAjaxConcepts)                                                                               |
| Manual             | [Session comparison](https://github.com/zaproxy/zap-core-help/wiki/HelpUiTlmenuReport#Compare_with_another_Session...)                                                         |
| Manual             | [Access Control Testing*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsAccessControlConcepts)                                                                      |
| Manual             | [HttpsInfo*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsHttpsinfoHttpsinfo)                                                                              |
| **A7**             | [A7 Cross-Site Scripting (XSS)](https://www.owasp.org/index.php/Top_10-2017_A7-Cross-Site_Scripting_(XSS))                                                                     |
| Automated          | [Active Scan Rules](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsAscan) ([Release](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsAscanrulesAscanrules) |
| Manual             | [Fuzzer](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsFuzz), combined with the [FuzzDb*](https://github.com/zaproxy/zap-extensions/wiki/AddOn_fuzzdb) files |
| Manual             | [Plug-n-Hack](https://github.com/zaproxy/zap-core-help/wiki/HelpAddonsPlugnhackPlugnhack)                                                                               |
| **A8**             | [A8 Insecure Deserialization](https://www.owasp.org/index.php/Top_10-2017_A8-Insecure_Deserialization)                                                                         |
| Automated          | There are two outstanding issues that are relevant to this Top 10 entry: [Insecure deserialization active scanner](https://github.com/zaproxy/zaproxy/issues/4112) & [Java Serialization Handling](https://github.com/zaproxy/zaproxy/issues/4509) |
| **A9**             | [A9 Using Components with Known Vulnerabilities](https://www.owasp.org/index.php/Top_10-2017_A9-Using_Components_with_Known_Vulnerabilities)                                   |
| Automated          | [Passive Scan Rules](https://github.com/zaproxy/zap-core-help/wiki/HelpStartConceptsPscan) ([Alpha*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsPscanrulesAlphaPscanalpha)) and Retire|
| Manual             | [Wappalyzer - Technology detection*](https://github.com/zaproxy/zap-extensions/wiki/HelpAddonsWappalyzerWappalyzer)                                                    |
| **A10**            | [A10 Insufficient Logging & Monitoring](https://www.owasp.org/index.php/Top_10-2017_A10-Insufficient_Logging%26Monitoring)                                                                                                                                          |
| Automated / Manual | The Spider(s), Active Scanner, Fuzzer, and Access Control addon can all be used to generate traffic and "attacks" which are potential sources/causes for logging and alerting. |
|                    |                                                                                                                                                                                |

&#42; The stared add-ons are not included by default in the full ZAP release but can be downloaded from the ZAP Marketplace via the ‘Manage add-ons’ button on the ZAP main toolbar.

![ZAP Toolbar - Marketplace Button](https://github.com/zaproxy/zap-extensions/wiki/images/zap-screenshot-browse-addons.png)
