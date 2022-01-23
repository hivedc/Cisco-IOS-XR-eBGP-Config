# Cisco-IOS-XR-eBGP-Config
Generic scalable eBGP config for IOS XR 

Hive has spent a bit of time doing trial and error to find the most scalable way of naming and configuring prefix sets and route policies.
Here is a short version of a generic config to simplify your first IOS XR BGP config.
Hopefully this will save you some time if you've never done BGP on Cisco IOS XR, which is very different from IOS XE.


## Possible improvements
- Put a prefix on elements, ex: add "rp-" before route-policies and "cs-" before community sets to identify them more easily

## Key takeaways
- no peer ASN name, only the ASN # (M&As happen all the time, ASNs change less often)
- WAN side prefix sets are not scalable. We only use prefix sets on the customer side and do the rest with BGP communities
