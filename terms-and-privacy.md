---
title: Terms and Privacy
description: >-
  What we're agreeing to and sharing
---
# Licenses and Terms-of-Use
This website and the dctransistor boards are Copyright (C) Logan Arkema 2023 for all original works. I am sharing the project under free and open-source licenses for community members who want to create their own projects with WMATA's API or use my board schematics for similar projects.

## Boards
When you purchase a DCTransistor board, you are *only purchasing the physical board*, not the software running it. While I make a reasonable effort to keep the software accurate and maintained over the long-term, I make no guarantees about the software's performance or my ability to provide live train positions into the future. The board's software may stop working at any time, for any reason. I will not, however, remove the open-source version of the software from GitHub for any reason that is under my control.

In addition, boards come as-is and are under no warranty. I will do my best to repair or replace broken boards if you ship them back to me, but this best-effort is not a guarantee or promise. If you have a broken board you would like me to try to fix, [contact me](/contact/). Boards do not include a power supply or any other supplementary materials.

I've licensed the boards themselves with a dual-licensing structure. An MIT license for the software (do what you want with it) and a Creative Commons-Attribution-NonCommercial-ShareAlike 4.0 license for the board design and schematics. More information is in the project's [license file](https://github.com/LArkema/dctransistor-project/blob/main/LICENSE.md). If you have questions, [contact me](/contact/).

The board software relies on a number of libraries and firmware, each of which is listed in the project's [bill of materials](https://github.com/LArkema/dctransistor-project/blob/main/bom.json).

### Local Pickup
I'm offering the local pickup option as a convenience for people I would already come across in-person as a way to build community in DC and reduce shipping costs (both financial and environmental). I cannot guarantee I can provide it on a widely available or continuing basis, and I reserve the right to offer it on a completely discretionary basis and refuse local pickup for any reason. You *must* arrange a local pickup by emailing <a href="mailto:orders@dctransistor.com">orders@dctransistor.com</a> before selecting the local pickup option at checkout, otherwise you will be responsible for any shipping costs.

### Website
This website is provided under a [MIT license](/LICENSE), and is based on the [Hydra Template](https://cloudcannon.com/community/themes/hydra/), which is also provided under an MIT license. Feel free to to use my website as the basis for your own, but do not imitate the actual content of this website in an attempt to impersonate or recreate this website for fraudulent or misleading purposes. 

### WMATA Licenses
This board is powered by data provided by WMATA's API, and I am using that data in compliance with [WMATA's Developer License Agreement / Transit Data Terms of Use](https://developer.wmata.com/license). 

The WMATA Metrorail System Map is (C) 2019 Washington Metropolitan Area Transit Authority ( (C) 2022 for map showing silver line extension and potomac yard station), and I make no claims on the original system map. The transformation of the map onto programmable circuit board (PCB) with light-emitting-diode (LED) station displays is (C) Logan Arkema 2023.

# Privacy Policy
*Update 4/3/23*: Added high level description of how data is processed when a board is purchased and link to open-source order handling code. Modified Stripe, USPS, and Google sections to describe how each service interacts with board order information. Added Shippo section to describe how it is used to ship board orders. 

The privacy of my visitors and potential board customers is extremely important to me. This Privacy Policy outlines the types of personal information that is received and collected and how it is used.

To the best of my ability, *I* collect the least amount of information necessary. I want you to enjoy your board - I don't really need to know anything about you beyond what it is necessary to sell you that board. This site does not have any built-in trackers or ways for me to know you were here. I may add a Google analytics tracker at some point to better understand how many people are visiting this website and get some understanding of potential customers. If I do so, this page will be updated.

When you buy a board, I automatically retrieve your order information from [Stripe](#stripe) to track financial information and then immediately generate a shipping label with [Shippo](#shippo) (for shipped orders). A week after your board is delivered, I delete all personally identifying information from your order except your zip code from my main business records (keeping the product description, shipping method, payment totals, zip code, and dates your board was ordered, shipped, and received so I can track financial records and shipping times). While Stripe and Shippo do not let me delete your order information from their databases in order to preserve business records, I do not access these records except when needed and do not download or share them from either site except in the manner described.

*Want to validate these claims?* [The code that does it all is on GitHub.](https://github.com/LArkema/dctransistor-project/blob/main/business_logic/order_handling.js)

In general, any information you provide for email lists, sales, or marketing purposes will not be shared or sold with anyone outside the services I use to run this website and service. I will only share the information needed to provide you with up-to-date information or complete an order, and will delete what I can soon after it is no longer necessary. While I will try to keep this page up-to-date with the different services I use and how I use them, that level of detail is not guaranteed. As a result, by using this website, providing information to me, or purchasing a board, you agree to the terms and conditions of whichever services I use as necessary for the purposes you provided the information. If you want me to delete any data that I have not done automatically and that the services I use let me delete, [contact me](/contact/).

### Stripe
I use [Stripe](https://stripe.com/privacy) for payments processing and ordering. After you submit an order, I retrieve your shipping address, shipping method, and total payment amount from Stripe and use it to generate a shipping label for your board with [Shippo](#shippo). Your address is processed when you order to automatically generate a shipping label, and is not stored in any other location except for your zip code. While Stripe does not allow me to manually delete your information (including the last four digits of your credit card number, shipping address, and IP address used to access the checkout page), I never download any additional information from Stripe and do not access it unless needed to resolve a dispute, maintain required business records, or fulfill another legal obligation put upon me. 

### Shippo
I use [Shippo](https://goshippo.com/privacy/) to generate USPS shipping orders, so your shipping address is necessarily shared with Shippo. If you consent to share your email address with Shippo for shipping updates, I will share your email address with them as well. While Shippo does not let me delete order information after it is generated from Shippo in order to preserve business records, I do not store a copy of your address other than your zip code for longer than a week after your board is delivered and I try to delete your shipping label from my computer soon after printing it. 

### USPS
I use the [United States Postal Service](https://about.usps.com/who/legal/privacy-policy/full-privacy-policy.htm) to ship boards to you. When I generate a shipping label with [Shippo](#shippo), your shipping address will necessarily be shared with USPS. If you consent to share your email address with Shippo for shipping updates, they may also share your email address with USPS. 

*First Class vs. Priority Shipping*: In addition to the expedited shipping for priority shipping, USPS also insures Priority Mail packages but not for First Class packages. All shipping insurance claims with your board should be directed to USPS.

### Google
I use Google Workspaces to manage the basic business side of DCTransistor (i.e. email, spreadsheets, and forms). When you submit an order, I use Google Workspaces to download your transaction details (product description, order total, shipment method, shipping address, and other Stripe-generated order data) from Stripe and to immediately generate a shipping label with Shippo for non-local pickup orders. I do not store any address information except for your zip code in Google Workspaces. Approximately a week after your board is delivered, Google Workspace automatically deletes any potentially personally-identifying information from your order and only preserves the product description, shipping method, payment amounts, zip code, and dates your board was ordered, shipped, and received to help me manage financial records and delivery times among different delivery methods. 

I may also use Google forms to manage email lists and waitlists (as I did with the preorder waitlist). As a result, when you visit a page with an embedded Google form, Google will likely know that you visited this website and that page. Further, Google may collect some information about your computer when you submit a form. Because the form goes to a paid Google Workspace account, Google should not be able to see any responses you submit. I only see what information you volunteer to submit in the form, and will delete all data from the form after everyone on the waitlist is contacted with sales information. 

Further, all emails are provided through a paid Google Workspace account. None of this data should be readable by Google other than to provide me access to my account. Based on information [provided by Google](https://workspace.google.com/security/?secure-by-design_activeEl=data-centers), an independent auditor (EY) verified Google Workspace privacy practices are compliant with multiple frameworks that require that customer data (what you share with me) belong to customers and are not used for anything other than to provide services to those customers.

### GitHub
This site is hosted on GitHub pages. As result, GitHub (owned by Microsoft) can view, and likely logs, information about your traffic to this site. This information generally includes:

* Internet Protocol (IP) addresses
* Types of browser
* Internet Service Provider (ISP)
* Date and time you visited
* Referring and exit pages
* Number of clicks

[GitHub's privacy statement](https://docs.github.com/en/github/site-policy/github-privacy-statement#github-pages), sparsely mentions that they may collect information, including IP addresses, from you by visiting this site.

In addition, your board connects to GitHub when it turns on to check for software updates and download them if one is available. As a result, GitHub will likely know that you own a DCTransistor board and that it is connecting from the public IP address of the network your board is connected to.

### WMATA
When you use a board, your board will connect to a WMATA API server, providing WMATA with the public IP address of the network the board is on. In addition, if you do not change the default WMATA API key I provide, your board
will contribute to an aggregated view of WMATA API use across all boards I sell. In practice, this will only let me know that you have connected your board to WMATA and which country you have connected it from. You can also [create your own WMATA key](https://developer.wmata.com/signup/) and put it onto your board to see the data for yourself.
