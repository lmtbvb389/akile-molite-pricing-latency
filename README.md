# akile molite: six plan prices, why a Macau IP sits in a Hong Kong rack, the measured China latency, and what to buy while stock reads zero (full table)

AkileCloud's MOLite line costs **CNY 24.99 to CNY 237.49 per month** across six KVM plans. Every one of them ships with one IPv4 and one IPv6 address, and every one carries a Macau broadcast IP on a machine that physically sits in Hong Kong. Checked on 8 November 2026, all six plans showed **zero stock** in the vendor's store data, and a third-party catalogue listed them as out of stock as well.

What follows is the full spec and price table, the two 10 Gbps unmetered SKUs that most people miss, what annual billing and traffic resets do to the real cost, and the measured latency of a Macau node on this network so you know what ping to expect before paying. If you only want the short version, it is below.

> **Quick pick.** Most readers want MOLite-Mini at **CNY 24.99/month** (1 vCPU, 1 GB RAM, 10 GB disk, 1 Gbps port, 2,500 GB traffic) because it is the cheapest way to get a Macau IP on this network. If you need the port speed rather than the IP, 高级竞技A at **CNY 50/month** gives you 10 Gbps and unmetered traffic. Stock is at zero right now, so open the order page, confirm availability, then pay.
> 👉 [Check MOLite stock and current pricing on the AkileCloud order page](https://akile.io/register?aff_code=24a6f6bd-f995-4158-a9fd-f4b6aef27811)

## MOLite plans and prices: all six SKUs

All six are KVM, all six get 1 IPv4 and 1 IPv6, and the disk sizes split into 10 GB and 20 GB. The difference that matters is the port and the traffic allowance, not the core count.

| Plan | vCPU / RAM / Disk | Port / monthly traffic | Monthly | Annual | Order |
| --- | --- | --- | --- | --- | --- |
| MOLite-Mini | 1 / 1 GB / 10 GB | 1 Gbps / 2,500 GB | CNY 24.99 | CNY 249.90 | [Order Mini](https://akile.io/register?aff_code=24a6f6bd-f995-4158-a9fd-f4b6aef27811) |
| MOLite-Starter | 1 / 1 GB / 10 GB | 2 Gbps / 5,000 GB | CNY 43.74 | CNY 437.40 | [Order Starter](https://akile.io/register?aff_code=24a6f6bd-f995-4158-a9fd-f4b6aef27811) |
| MOLite-高级竞技A (Advanced Gaming A) | 1 / 1 GB / 10 GB | 10 Gbps / unmetered | CNY 50.00 | not offered | [Order Gaming A](https://akile.io/register?aff_code=24a6f6bd-f995-4158-a9fd-f4b6aef27811) |
| MOLite-高级竞技B (Advanced Gaming B) | 2 / 2 GB / 10 GB | 10 Gbps / unmetered | CNY 90.00 | not offered | [Order Gaming B](https://akile.io/register?aff_code=24a6f6bd-f995-4158-a9fd-f4b6aef27811) |
| MOLite-Standard | 2 / 1 GB / 20 GB | 2 Gbps / 10,000 GB | CNY 99.99 | CNY 999.90 | [Order Standard](https://akile.io/register?aff_code=24a6f6bd-f995-4158-a9fd-f4b6aef27811) |
| MOLite-Pro | 2 / 2 GB / 20 GB | 2 Gbps / 30,000 GB | CNY 237.49 | CNY 2,374.90 | [Order Pro](https://akile.io/register?aff_code=24a6f6bd-f995-4158-a9fd-f4b6aef27811) |

The two 高级竞技 plans report a traffic value of 0 in the store data and carry a reset price of 9,999,999, which is how the store marks an unmetered plan. AkileCloud's own launch material for this series described both as unmetered on a 10 Gbps port, and that matches. The four cheaper-to-mid plans are metered, and running over means buying a traffic reset.

Two things worth noticing in that table. **10 Gbps is only available on the two gaming SKUs.** Mini, Starter, Standard and Pro top out at 1 or 2 Gbps. And Standard at CNY 99.99 gives you a second core but leaves you at 1 GB of RAM, the same memory as the CNY 24.99 plan.

## What annual billing and traffic resets add to the bill

Annual billing is offered on the four metered plans only, and the discount is identical across all of them: you pay for ten months and get twelve.

| Plan | Monthly × 12 | Annual price | Saving | Traffic reset fee |
| --- | --- | --- | --- | --- |
| MOLite-Mini | CNY 299.88 | CNY 249.90 | CNY 49.98 (16.7%) | CNY 20.00 |
| MOLite-Starter | CNY 524.88 | CNY 437.40 | CNY 87.48 (16.7%) | CNY 36.00 |
| MOLite-Standard | CNY 1,199.88 | CNY 999.90 | CNY 199.98 (16.7%) | CNY 70.00 |
| MOLite-Pro | CNY 2,849.88 | CNY 2,374.90 | CNY 474.98 (16.7%) | CNY 144.00 |

The reset fee scales with the plan, and on Pro it is **CNY 144 per refill**. If you expect to burn through 30 TB regularly, that number belongs in your budget alongside the subscription, because a single reset costs more than half of a Mini subscription. Only the current prices are published; nothing in the store data indicates what a renewal will cost later, so treat the annual figure as the price for that term rather than a permanent rate.

👉 [Start with the annual MOLite-Mini plan at CNY 249.90](https://akile.io/register?aff_code=24a6f6bd-f995-4158-a9fd-f4b6aef27811)

## Why an akile molite plan shows a Macau IP from a Hong Kong rack

The store's own plan description says it plainly: **"澳门广播IP 机器位置在HK"**, a Macau broadcast IP with the machine located in Hong Kong. The launch coverage for this series said the same thing, that MOLite uses Macau broadcast IPs while the physical server stays in Hong Kong. One VPS directory files MOLite under Hong Kong for exactly this reason, which is where a lot of the confusion about this line comes from.

A broadcast IP means the address block is registered to Macau and announced from a network that sits in Hong Kong. What you get out of it:

- Geo-IP lookups, sign-up forms and regional catalogues will usually read your server as being in Macau.
- The actual packet path starts in Hong Kong, so latency to Macau services is not what a Macau-racked machine would give you, and latency to the mainland follows a Hong Kong route.
- The address is shared infrastructure, not a dedicated block, so it is worth testing whatever service you care about during the refund window rather than assuming it will behave.

If your reason for buying is "I need an IP that reads as Macau", this is the product. If your reason is "I need a server in Macau", it is not, and no amount of plan comparison will change that.

## Measured latency: what ping a Macau node on this network returns

The most useful public measurement of a Macau machine on AkileCloud's network comes from a 6 November 2026 test of **MFM.MOLite.One**, a separate promotional machine priced at CNY 69.90 per year with 1 vCPU (Xeon Gold 6133), 0.9 GB RAM, 4.8 GB disk, a 5 Gbps port and 1 TB per month. It is not one of the six plans above, and its price and specs should not be read as MOLite-Mini's. Use it as a reference for the latency magnitude of a Macau node here.

Median latency in milliseconds, by city and carrier:

| City | China Telecom (163) | China Unicom (4837) | China Mobile (CMI) |
| --- | --- | --- | --- |
| Beijing | 310 | 329 | 190 |
| Shanghai | 297 | 257 | 181 |
| Zhejiang | 339 | 264 | 183 |
| Jiangsu | 317 | 261 | 190 |
| Guangdong | 323 | 336 | 171 |
| Hubei | 320 | 266 | 192 |
| Sichuan | 349 | 228 | 197 |

China Mobile's CMI return path is the best of the three at **171–197 ms**. Unicom on 4837 sits in the middle at **228–336 ms**. Telecom on 163 is the worst, running **297–349 ms** across every city tested.

That pattern tells you this node has no mainland three-network optimisation. AkileCloud labels its JPPro line explicitly as 大陆三网优化, three-network optimised for the mainland; MOLite carries no such label anywhere in its store entry. The 300 ms-plus Telecom figures are the kind of number you get from international transit plus a Macau-registered address, not from a premium China route.

So: if you need interactive SSH from a mainland Telecom connection, expect a sluggish session. If you need a Macau IP for a service that checks registration country, or a cheap high-port-speed box for international traffic, the latency is irrelevant to the job.

👉 [See the Macau MOLite plans on the AkileCloud order page](https://akile.io/register?aff_code=24a6f6bd-f995-4158-a9fd-f4b6aef27811)

## Picking a plan by workload

**You want a Macau IP and not much else.** Mini, CNY 24.99. 2,500 GB on a 1 Gbps port covers a single site, an API endpoint, or a region-locked account. Nothing cheaper in this line exists.

**You want port speed and no traffic meter.** 高级竞技A at CNY 50, or B at CNY 90 if you need 2 GB of RAM. These are the only two plans with 10 Gbps and unmetered traffic, and neither has an annual option, so you pay monthly.

**You think you need Standard. Check Gaming B first.** Standard costs CNY 99.99 for 2 vCPU, 1 GB RAM, 20 GB disk, 2 Gbps and 10 TB. Gaming B costs CNY 90 for 2 vCPU, 2 GB RAM, 10 GB disk, 10 Gbps and unmetered traffic. Unless the extra 10 GB of disk is the deciding factor, Gaming B is the better buy on every other axis, and it is cheaper. Standard's 1 GB of RAM on a 2-core box is an awkward pairing for anything memory-hungry.

**You need 30 TB.** Pro at CNY 237.49, and budget CNY 144 for each reset beyond that. Below Pro, the largest allowance is Standard's 10 TB.

## Everything is out of stock. What now?

All six plans read zero when checked, and the third-party directory agrees. That is the single most important fact on this page: **you cannot buy MOLite today just because the price is listed.** The series launched around May 2026 and the vendor has not published a restock schedule, so the practical move is to open the order page and look at live availability rather than waiting on a rumour.

If you need something running this week, these are the same-brand alternatives that actually showed stock at the same check:

- **TWLite-Mini, CNY 24.99, 20 in stock.** 2 GB RAM, Taiwan, described in the store as having no mainland optimisation with DNS unlock for Taiwan streaming. Same price as MOLite-Mini, twice the memory, different geography.
- **JPIIJ-Starter, CNY 48.60, 19 in stock.** 1 vCPU, 1 GB RAM, 20 GB disk, 1 Gbps, 2,000 GB.
- **JPIIJ-Standard, CNY 98.60, 20 in stock.** 5,000 GB on a 1 Gbps port.
- **JPHyper-Pro, CNY 289.99, 20 in stock.** 2 vCPU, 4 GB RAM, 30 TB, with the store listing GSL, PCCW, COGENT, EIE and TATA transit plus DNS-based unlocking for Netflix, Disney+, YouTube, ChatGPT, Abema and DMM.

Two alternatives that look right on price but are also sold out: JPIIJ-Lite at CNY 24.99 (1 GB RAM, 10 GB disk, 1,000 GB traffic, 1 Gbps) and the whole JPPro range except the CNY 447.50 Ultra.

## FAQ

**Does a Macau IP mean the server is in Macau?** No. The store description and the launch coverage both say the machine is in Hong Kong and only the IP is Macau-registered.

**Is IPv6 included?** Yes, one address per plan across all six SKUs, alongside one IPv4.

**What happens when I hit the traffic limit?** The store lists a reset fee for each metered plan (CNY 20 / 36 / 70 / 144). No throttling rule is published on the plan pages, so if you are close to the limit, ask support what happens before you order rather than after.

**Can I get a refund?** Third-party summaries of AkileCloud's service agreement describe refunds credited to account balance only, available within 24 hours of provisioning if no more than 5 GB of traffic has been used, capped at three machines per account per calendar month, and excluding discounted or coupon purchases entirely. Those terms are not shown on the plan pages themselves, so confirm with support before paying, especially on an annual order.

**Which operating systems are available?** Debian 11, 12 and 13; Ubuntu 18.04, 20.04 and 22.04; Rocky Linux 8 and 9. Virtualisation is KVM throughout.

**Is 10 Gbps available on the cheap plans?** No. Mini is 1 Gbps, Starter and the two larger metered plans are 2 Gbps, and 10 Gbps is exclusive to 高级竞技A and B.

## Three rules before you order

1. **Buy MOLite for the address, not the ping.** Telecom returns of roughly 300–350 ms are normal here. If your workload needs low mainland latency, this is the wrong line, and the vendor's own optimised series carries a different label.
2. **Compare Gaming B against Standard before defaulting to the bigger number.** CNY 90 buys 2 GB of RAM, 10 Gbps and no traffic meter; CNY 99.99 buys 1 GB of RAM, 2 Gbps and 10 TB. Only the disk size favours Standard.
3. **Confirm stock and intended use first.** All six plans read zero, and the plan pages do not spell out streaming or proxy permissions, so get a written answer from support before committing to an annual term.

👉 [Open the AkileCloud order page and check MOLite availability](https://akile.io/register?aff_code=24a6f6bd-f995-4158-a9fd-f4b6aef27811)
