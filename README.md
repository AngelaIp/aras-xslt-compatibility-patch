# aras-xslt-compatibility-patch
Unofficial compatibility patch for older Aras Innovator releases affected by browser XSLT processor removal.

# Disclaimer
This repository is an unofficial community effort and is not affiliated with, endorsed by, or supported by Aras Corporation.

No original Aras Innovator source files are distributed through this repository.
Only the required modifications and implementation details are documented.

Aras Innovator is a trademark of Aras Corporation.


# Failure Scenario 
Behavior Without the XSLT Patch - Test with Chrome Canary Version 159.0.8146.0 (Offizieller Build) canary (64-Bit)
<img width="1009" height="555" alt="image" src="https://github.com/user-attachments/assets/8181d61d-fcc3-46e4-9320-41dd4bbb4e9f" />


# Solution 1 - Temporary Browser-Based Workaround
As a temporary mitigation, affected users can re-enable the deprecated XSLT processor in Chrome-based browsers using the corresponding browser flag.

<img width="1009" height="417" alt="image" src="https://github.com/user-attachments/assets/ae85e3fb-807f-4a0c-bd37-0c45fbdee0d7" />

> [!IMPORTANT] 
> This workaround is only intended as a short-term solution. Browser vendors have announced the removal of native XSLT processing, and the flag may be removed in a future browser release without further notice.

By enabling the XSLT-related flag, older Aras Innovator releases can continue to operate without any server-side modifications for a limited period of time. However, this approach should only be used as an interim measure while preparing and validating a long-term solution.



# Solution 2 - XSLT Polyfill Patch

> [!WARNING]
> Important Notice
> The solution described in this document is an unofficial patch and is not approved or supported by Aras.
> Applying this patch may have unintended side effects and could affect future upgrades or supportability.
> Use of this patch is entirely at your own discretion and risk.
> For production environments, we recommend relying on officially supported fixes provided through an active Aras subscription.

### Add file xslt-polyfill.min.js to folder ..\Innovator\Client\vendors
Get file from https://github.com/mfreed7/xslt_polyfill/ or Release 2026.
