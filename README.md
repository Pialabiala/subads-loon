# subads-loon

Loon plugin to block ad delivery observed in the supplied SubLife HAR.

## Install

Add this URL in Loon:

`https://raw.githubusercontent.com/Pialabiala/subads-loon/main/sub.plugin`

The plugin blocks the app's `/fem/api/advertisement/findList` endpoint, the ad SDK / bidding hosts observed in the capture, plus Pangle configuration and ByteDance playable ad assets observed in the follow-up HAR.

The HAR shows application-layer encrypted responses from `sublifeapp.com`, so this plugin does not rewrite the app's encrypted home/config payloads. Some first-party campaign assets may still load if the app embeds them in those responses.

This plugin only targets ad delivery. It does not bypass account, subscription, or paid-feature restrictions.
