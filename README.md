# VPS for forex trading: how much RAM your MT4/MT5 setup needs, which datacenter to pick, and what JustHost's standard NVMe plans cost from $1.99 to $27.94 a month

A forex VPS for one or two MT4 terminals costs about $5 to $8 a month at JustHost. The 2 GB Double Star plan is $7.08 monthly, or $5.67 per month on 12-month billing. The more expensive mistake is choosing the wrong city: a 4 GB server in the wrong datacenter will fill worse than a 2 GB server next to your broker's matching engine.

This guide covers JustHost's current NVMe plans, the RAM-to-terminal ratio, how to read your broker's server list to pick a location, and the billing, Windows, and refund details to confirm before you pay.

> **Most readers should start with Double Star.** 2 vCPU, 2 GB RAM, 20 GB NVMe, 200 Mbps port. $7.08/month, or $5.67/month on 12 months. It runs one or two MT4 terminals or one MT5 terminal with a few charts. If you run three or four terminals, go to Bright Star at $9.80/month ($7.84 on 12 months).
>
> 👉 [Check the Double Star plan and current 12-month price](https://justhost.asia/en/services/vps/tariffs/double-star-c2r2048nvme?ref=196392)

## JustHost VPS plans compared

JustHost's standard NVMe line starts at $1.99/month for a 512 MB promo box and tops out at $27.94/month for 4 cores, 8 GB RAM, and 200 GB NVMe. The table below uses the monthly and 12-month rates shown on JustHost's tariff page. The 12-month column is an effective monthly rate, not the total due today: multiply by 12.

| Plan | vCPU / RAM | NVMe / port | Monthly | 12-month (per month) | Order |
| --- | --- | --- | ---: | ---: | --- |
| VPS Promo | 1 core / 512 MB | 5 GB / 10 Mbps | $1.99 | not shown | [ VPS Promo](https://justhost.asia/en/services/vps/tariffs/promo-c1r512nvme?ref=196392) |
| New Star | 1 core / 1 GB | 10 GB / 100 Mbps | $3.81 | $3.05 | [ New Star](https://justhost.asia/en/services/vps/tariffs/new-star-c1r1024nvme?ref=196392) |
| Double Star | 2 cores / 2 GB | 20 GB / 200 Mbps | $7.08 | $5.67 | [ Double Star](https://justhost.asia/en/services/vps/tariffs/double-star-c2r2048nvme?ref=196392) |
| Bright Star | 4 cores / 4 GB | 30 GB / 300 Mbps | $9.80 | $7.84 | [ Bright Star](https://justhost.asia/en/services/vps/tariffs/bright-star-c4r4096nvme?ref=196392) |
| Sirius | 1 core / 1 GB | 20 GB / 300 Mbps | $4.85 | $3.88 | [ Sirius](https://justhost.asia/en/services/vps/tariffs/sirius?ref=196392) |
| Arcturus | 1 core / 2 GB | 30 GB / 300 Mbps | $6.92 | $5.53 | [ Arcturus](https://justhost.asia/en/services/vps/tariffs/arcturus?ref=196392) |
| Alpha Centauri | 2 cores / 2 GB | 40 GB / 400 Mbps | $8.99 | $7.19 | [ Alpha Centauri](https://justhost.asia/en/services/vps/tariffs/alpha_centauri?ref=196392) |
| Vega | 2 cores / 4 GB | 80 GB / 500 Mbps | $13.44 | $10.75 | [ Vega](https://justhost.asia/en/services/vps/tariffs/vega?ref=196392) |
| Capella | 4 cores / 4 GB | 120 GB / 750 Mbps | $18.30 | $14.64 | [ Capella](https://justhost.asia/en/services/vps/tariffs/capella?ref=196392) |
| Rigel | 4 cores / 8 GB | 200 GB / 750 Mbps | $27.94 | $22.35 | [ Rigel](https://justhost.asia/en/services/vps/tariffs/rigel?ref=196392) |

VPS Promo is included for completeness, not as a recommendation. 512 MB of RAM is below what MT4 needs once you add a few charts and an EA.

### JustHost's promotional “Special” configurations

JustHost also shows a separate “Special” price on several configurations. These are the same resource classes under a promotional label, not a different architecture. Check the cart for the term required and whether the price still applies.

| Plan | vCPU / RAM | NVMe / port | Monthly | 12-month (per month) | Order |
| --- | --- | --- | ---: | ---: | --- |
| Sirius Special | 1 core / 1 GB | 20 GB / 300 Mbps | $2.81 | $2.25 | [ See current price](https://justhost.asia/en/services/vps/tariffs-all?ref=196392) |
| Arcturus Special | 1 core / 2 GB | 30 GB / 300 Mbps | $4.01 | $3.21 | [ See current price](https://justhost.asia/en/services/vps/tariffs-all?ref=196392) |
| Vega Special | 2 cores / 4 GB | 80 GB / 500 Mbps | $7.79 | $6.23 | [ See current price](https://justhost.asia/en/services/vps/tariffs-all?ref=196392) |
| Yildun Special | 4 cores / 8 GB | 200 GB / 750 Mbps | $16.20 | $12.96 | [ See current price](https://justhost.asia/en/services/vps/tariffs-all?ref=196392) |
| Betelgeuse Special | 6 cores / 12 GB | 400 GB / 750 Mbps | $26.40 | $21.12 | [ See current price](https://justhost.asia/en/services/vps/tariffs-all?ref=196392) |
| Altair Special | 8 cores / 24 GB | 600 GB / 750 Mbps | $47.40 | $37.92 | [ See current price](https://justhost.asia/en/services/vps/tariffs-all?ref=196392) |

JustHost's VPS page also lists HDD, SSD, and IPv6-only variants. For MT4/MT5, the NVMe line is the one to compare. A 2-core/2 GB HDD plan at $11/month and the same RAM on SSD at $13.20/month are cheaper than NVMe, but the platform writes tick data and logs continuously. The I/O saving is not worth it on a trading server.

## Pick the datacenter before the plan

Your broker's trading server is in a specific building. The VPS needs to be in the same city, ideally the same Equinix campus. Broker server information collected in October 2026 puts IC Markets, FP Markets, Axi, and Global Prime in Equinix NY4; FxPro, Admirals, Darwinex, and BlackBull in LD4 or LD5; FXTM in Frankfurt. Exness is in Amsterdam, so compare Frankfurt and London ping rather than assuming one is closer.

Brokers move servers, and some run different platforms or entities in different cities. Check the exact server name in your platform before you order.

### How to check your broker's server location

1. Open the MT4 or MT5 login dialog. The server list shows the ping to every server your broker offers.
2. The lowest number is the server to measure your VPS against.
3. The connection status in the bottom-right corner of the terminal shows the ping to your current trade server.
4. Ask your broker for the data center name if it is not public. Most use Equinix sites such as NY4, LD4, FR2, or SG1.

The JustHost plan table does not list datacenter cities or map them to Equinix sites. Ask support which location is closest to your broker's server and request a test IP. If they cannot name the city or provide an IP to ping, you are buying blind on the one variable that matters most.

👉 [Compare JustHost's VPS plans and then confirm the city with support](https://justhost.asia/en/services/vps/tariffs-all?ref=196392)

## How much RAM does an MT4 or MT5 terminal need?

Plan for 512 MB to 1 GB of RAM per MT4 instance. A 2 GB server runs one or two MT4 terminals. 4 GB runs three or four comfortably. 8 GB covers five to eight. 16 GB is for ten or more. MT5 is 64-bit and uses more memory per terminal. The Strategy Tester will consume every vCPU you give it, so do not run backtests on the same 2 GB box as live EAs.

| What you run | RAM to plan | JustHost plan |
| --- | --- | --- |
| One MT4 terminal, a few charts | 1–2 GB | Arcturus or Double Star |
| Two or three MT4 terminals, or one MT5 with several charts | 2–4 GB | Double Star or Bright Star |
| Four to six terminals plus a copier | 4–8 GB | Vega, Capella, or Rigel |
| Eight or more terminals, or backtesting while trading | 8–16 GB+ | Rigel or a larger tier |

ForexVPS.net uses a more conservative ratio: its 4 GB Core plan is rated for up to three MT4/5 terminals, the 6 GB Edge for up to six, and the 8 GB Prime for six or more, all “if optimised.” If you run many indicators, use that ratio rather than 512 MB per terminal. Indicators consume more resources than EAs, and stacking them is the usual reason a 2 GB box runs out of memory.

👉 [Check the Bright Star plan if you need 4 GB for two or three terminals](https://justhost.asia/en/services/vps/tariffs/bright-star-c4r4096nvme?ref=196392)

## Shared vCPU or dedicated cores?

JustHost's table lists vCPU cores but does not describe them as dedicated. Assume shared unless support confirms otherwise. Shared CPU is fine for one to four MT4 terminals running EAs that trade a few times a day. Dedicated cores matter when you run multiple EAs across many pairs, a copier, or a strategy that reacts to news releases.

The price gap is real. MassiveGRID's shared Forex VPS starts at $2.87/month; its dedicated-CPU Forex VPS Pro starts at $9.73. ForexVPS.net's shared Prime is $72/month; its dedicated server is $270/month. If you need guaranteed CPU, you are comparing a different class of provider, and JustHost's published line does not compete there.

Most retail setups do not need dedicated cores. A single MT4 with two EAs, swing trading, or a copier with a handful of accounts will run fine on shared vCPU. Pay for dedicated cores when a missed execution or a delayed exit costs more than the monthly difference.

## The real monthly cost: 12-month pricing, renewals, and promotional labels

The 12-month column is an effective monthly rate. Double Star at $5.67/month on 12 months means about $68 upfront. The monthly price is $7.08. That is a 20% difference. JustHost offers the 12-month rate when you order three months or more on the plans where it is shown. Check the cart total, because the displayed monthly rate and the amount charged today are different numbers.

Contabo's forex page is explicit that its displayed prices are “for the first 24 months.” The renewal rate is the number to check. JustHost's table does not show a separate renewal rate; the monthly rate is the one to use for year two if you do not renew on a long term. QuantVPS advertises a three-year price lock, which protects against increases but locks you into that provider's pricing. A low first-term price is not a low three-year cost.

👉 [Check the 12-month total on the Double Star plan before you commit](https://justhost.asia/en/services/vps/tariffs/double-star-c2r2048nvme?ref=196392)

## Refund windows and uptime credits

JustHost's VPS plan table does not show a money-back period. Ask support for the refund window in writing before you pay, and confirm whether it starts at order or at activation. For context, MassiveGRID offers 15 days, ForexVPS.net 14 days, and QuantVPS 14 days. Those are refund windows, not uptime guarantees.

SLA credits are not refunds. QuantVPS's 99.999% SLA pays a 10% credit from the first failed minute. QuantVPS's own comparison table shows a competitor starting credits at 21.6 minutes with 5%, and another excluding credits in its terms. MassiveGRID advertises a 100% uptime SLA and HA failover. If your EA trades through news, a one-minute outage can cost more than the credit, so ask what happens to the VM during a node failure, not just what the percentage says.

## How JustHost compares on price

The table below uses published entry prices and plan prices. It is a price-and-positioning check, not a full feature comparison.

| Provider | Entry price | What you get | Check before buying |
| --- | --- | --- | --- |
| MassiveGRID | $2.87/mo | 1 vCPU, 2 GB RAM, 32 GB NVMe; New York, London, Frankfurt, Singapore; Windows; 15-day refund | Entry is shared CPU; Pro with dedicated cores starts at $9.73/mo |
| ForexVPS.net | $36/mo promo for Core | 4 GB RAM, 100 GB storage; 14-day refund; trade copier | Homepage says “from $28.80”; plan page's lowest promo is $36. Ask which configuration the $28.80 refers to |
| QuantVPS | $29.99/mo | New York or London (LD4); 99.999% SLA; 14-day refund; 3-year price lock | Higher entry price; dedicated resources are the selling point |
| Contabo | First 24 months pricing | 4 vCPU/8 GB and larger; Windows Server included | Displayed price is first-term; renewal rate is not in the price line |

JustHost's advantage is the bottom of the market. A 2 GB KVM box with NVMe and a 200 Mbps port for $5.67/month on 12 months is cheap. The trade-off is that the plan table leaves Windows licensing, datacenter mapping, and refund terms for you to confirm.

## Which JustHost plan fits your setup?

**One MT4 terminal, one or two EAs, swing trading:** Arcturus at $6.92/month ($5.53 on 12 months) or Double Star at $7.08 ($5.67). The extra core on Double Star costs $0.16/month. Take it.

**Two or three MT4 terminals, or one MT5 with several charts:** Bright Star at $9.80 ($7.84). If you keep years of tick data or run a copier, Vega at $13.44 ($10.75) adds 80 GB and a 500 Mbps port.

**Four to six terminals plus a copier:** Capella at $18.30 ($14.64) or Rigel at $27.94 ($22.35). Rigel's 8 GB is the safer choice if you run MT5 or several indicators.

**More than eight terminals or backtesting:** Rigel or larger. Do not run the Strategy Tester on the same box as live EAs.

**Need dedicated CPU:** JustHost's published line does not offer it. Compare MassiveGRID Pro or a dedicated server.

## Before you pay

- Confirm Windows: Is Server 2019 or 2022 available, and is the licence included? The tariff table does not show a Windows line.
- Confirm the datacenter city and ask for a test IP. Match it to the lowest-ping server in your MT4/MT5 login dialog.
- Confirm the refund window and its start date. The plan page does not publish one.
- Confirm the 12-month total and the renewal rate. The 12-month column is a monthly rate, not the upfront amount.
- Confirm whether the “Special” price applies to your term. The standard monthly price is the fallback.

👉 [Start with the Double Star plan if you run one or two MT4 terminals](https://justhost.asia/en/services/vps/tariffs/double-star-c2r2048nvme?ref=196392)
