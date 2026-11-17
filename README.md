# RackNerd VPS: Which Annual Plan Fits Your Workload, Does the Price Hold on Renewal, and Where the $21.99 Box Stops Being Enough (Full 5-Plan Table)

RackNerd's annual KVM VPS specials start at **$21.99/year** for 1 vCPU, 1 GB RAM, 20 GB SSD and 3 TB of monthly transfer, and top out at **$119.99/year** for 7 vCPU, 8 GB RAM, 150 GB SSD and 20 TB. Every tier in between ships with full root access, one dedicated IPv4, RAID-10 SSD storage behind a 1Gbps port, RackNerd's own ctrl control panel, and provisioning that completes within minutes of payment.

The detail that decides whether these prices are actually cheap: the specials are lifetime recurring, so the second year bills at the same rate as the first. Most budget providers hook you at $20 and renew you at $60. RackNerd's FAQ states the specials renew at the same price for as long as you keep the service.

> **Quick picks.** Most people self-hosting a VPN, a small site, n8n or a Docker stack should take the **2 GB plan at $35.99/year** (RackNerd labels it the most popular for a reason). Running Ollama with Open WebUI, LibreChat, AnythingLLM or Hermes Agent requires **4 GB at $59.99/year**. OpenClaw needs **8 GB at $119.99/year** and nothing smaller will do.
> 👉 [Check current RackNerd VPS specials and pricing](https://bit.ly/RacKnerd)

## The five annual plans, side by side

| Plan | vCPU / RAM / SSD | Monthly transfer | Price (annual) | Order |
| --- | --- | --- | --- | --- |
| 1 GB KVM VPS | 1 vCPU / 1 GB / 20 GB SSD | 3 TB @ 1Gbps | $21.99/yr | [Start with the 1 GB annual plan](https://bit.ly/RacKnerd) |
| 2 GB KVM VPS | 2 vCPU / 2 GB / 35 GB SSD | 5 TB @ 1Gbps | $35.99/yr | [Get the 2 GB plan most buyers choose](https://bit.ly/RacKnerd) |
| 4 GB KVM VPS | 3 vCPU / 4 GB / 60 GB SSD | 7 TB @ 1Gbps | $59.99/yr | [Order the 4 GB plan for local AI apps](https://bit.ly/RacKnerd) |
| 6 GB KVM VPS | 6 vCPU / 6 GB / 100 GB SSD | 12 TB @ 1Gbps | $89.99/yr | [Compare the 6 GB plan](https://bit.ly/RacKnerd) |
| 8 GB KVM VPS | 7 vCPU / 8 GB / 150 GB SSD | 20 TB @ 1Gbps | $119.99/yr | [Take the 8 GB plan for OpenClaw](https://bit.ly/RacKnerd) |

Notes on the table. The 4 GB tier carries 3 vCPU cores, which is worth flagging because a few third-party pages list it as 2; RackNerd's own specials page says 3. The jump from 4 GB to 6 GB doubles core count and adds 40 GB of disk for $30 more per year, which is the largest single step in resources anywhere in the lineup. If you expect to grow into a heavier stack within a year, that step is the one to think about now rather than later, since upgrading means a reboot and a short maintenance window.

Every plan allows one IPv4 address. Multiple IPv4s are not part of these packages. If you need a second address for mail separation or per-service routing, ask support before you buy rather than after.

## Match the plan to the app you're actually going to run

This is where most RackNerd reviews stay vague. The ctrl panel has a one-click app catalog, and each app has a documented minimum, so you can pick a plan from the software rather than guessing at specs.

- **OpenClaw:** 4+ vCPU and 8+ GB RAM. That means the 8 GB tier at $119.99/year is the only qualifying plan in the specials lineup.
- **Hermes Agent, AnythingLLM, Ollama (with Open WebUI as the chat front end), LibreChat:** 2+ vCPU and 4+ GB RAM. Start at 4 GB, $59.99/year. The 1 GB and 2 GB boxes will install and then fall over once a model loads.
- **n8n and Coolify:** 2+ vCPU and 2+ GB RAM, so 2 GB at $35.99/year covers a single-user instance. RackNerd's own guidance says to go to 4 GB when you add Postgres, a reverse proxy, or production workflows with AI tool connections. That is realistic advice: n8n with a database and a couple of busy workflows will use 2 GB before you notice.
- **AdminBolt:** 2+ vCPU, 2 GB RAM, installs on AlmaLinux 9, includes a 30-day free trial. The 2 GB plan is the entry point.
- **Portainer:** 1 vCPU and 2 GB is comfortable. **Webmin, CyberPanel and WireGuard (wg-easy):** 1 vCPU and 1 GB is enough, so the $21.99 plan genuinely works as a VPN box or a single-site server.

👉 [See the 4 GB plan that covers Ollama, LibreChat and AnythingLLM](https://bit.ly/RacKnerd)

Two things about the one-click installer that the app list doesn't tell you. An install takes roughly **15 to 45 minutes**, and it reinstalls the OS first, which **permanently erases everything currently on the VPS**. Running it on a box that already holds data is destructive by design. The second: credentials for the app appear in ctrl when the install finishes, so there is no separate dashboard to hunt down.

If the app you want isn't in the catalog, that costs you nothing. These are full-root KVM servers, so SSH, Docker and Compose work exactly as they would on any other VPS. RackNerd publishes an interactive ctrl demo you can click through without an account, including a 4-core/8 GB demo host and a 2-core/4 GB one, which is a reasonable way to see the panel before spending anything.

## Renewal pricing, and one counterintuitive comparison

A $21.99 annual VPS is only cheap if it stays $21.99. Three years on the 1 GB plan comes to about $66; three years on the 2 GB plan comes to about $108. Set that against the monthly-billed standard KVM line and the gap gets wide fast.

The odd part: RackNerd's standard KVM entry plan is **$26.99/year** for 512 MB RAM, 1 vCPU, 30 GB SSD and 500 GB of transfer with one dedicated IPv4. That is more money than the $21.99 special, for half the RAM and one-sixth the bandwidth. There is no configuration reason to pick the 512 MB standard plan over the 1 GB special unless you specifically need something the standard line includes and the specials don't. The standard line does scale higher and offers flexible billing cycles, up to 12 GB RAM, 7 vCPU, 300 GB of storage and 6 TB of transfer, but at that point you're comparing against the 8 GB special at $119.99/year, not against the entry tier.

One caveat on payment and cancellation. A widely circulated third-party guide mentions a 3-day refund window and one free IPv4 change within the first 72 hours. Neither of those appears on RackNerd's specials page or ordering documentation, so treat them as unconfirmed and open a ticket to ask before you pay if a trial period matters to your decision. Payment methods accepted include PayPal, credit card, cryptocurrency and wire transfer.

## The five things that catch first-time buyers

**It is unmanaged.** You get root and a panel. You do not get someone to configure Nginx, tune MySQL or debug your Docker networking. Support handles the platform: power, reinstalls, console access, the network firewall, and hardware. RackNerd runs 24/7 ticket support and its ordering guide quotes an average first response under 10 minutes.

**ctrl and the client area are two different logins.** The client area (billing, invoices, tickets) is separate from ctrl (the server itself). Your ctrl credentials arrive in an email titled "KVM VPS Login Information," and you can retrieve it later from View Email Log inside the client area. People lose an hour to this every week.

**Custom ISOs need a ticket.** The standard templates cover CentOS, Rocky Linux, AlmaLinux, Fedora, Debian and Ubuntu. Anything else, including FreeBSD or a Windows ISO, goes through a support request. Later reinstalls and out-of-band access happen through ctrl's HTML5 VNC console, which also works when SSH is broken.

**1Gbps is the port speed, not your download speed.** It describes the datacenter uplink. Your real throughput is capped by the slowest link between you and the facility, and a residential connection in Asia will not see anything close to a gigabit from Los Angeles.

**The network firewall is inbound-only.** ctrl's firewall rules handle incoming traffic. Outbound filtering and anything more elaborate belongs inside the OS.

👉 [Open a RackNerd VPS in the location you need](https://bit.ly/RacKnerd)

## Datacenters and free IPv6

RackNerd advertises 20 datacenter locations. The ones named on its own ordering documentation include Los Angeles (DC-02 and DC-03), San Jose, Seattle, Dallas, Atlanta, Chicago, New York, Ashburn, Amsterdam, France and Dublin, with additional North American and European sites listed elsewhere.

Location will change how fast a server feels more than an extra vCPU core will. A 2 GB box in a facility 30ms from your users beats a 4 GB box 200ms away for anything interactive. Before ordering, ping the test IP for the facility you're considering from the network your users are on. Under 100ms is comfortable for interactive apps; under 200ms is fine for most web workloads. For traffic coming from Asia, Los Angeles DC-02 is the usual first choice on RackNerd's network.

IPv6 is available by ticket: up to **100 free IPv6 addresses** in the Los Angeles and France locations, with more locations planned. That is enough to give every container or service its own address and leave the single IPv4 for what actually requires it. You have to open the ticket after ordering; it isn't automatic at checkout.

## What buyers actually report

Trustpilot shows **4.1 out of 5 across 371 reviews** in the snapshot displayed on the RackNerd Club page. The recurring themes in the reviews that page quotes: a PTR/rDNS change handled in about 10 minutes on the $35.99 2 GB promo, port 25 left unblocked (uncommon among providers that stay in business), 100% uptime on UptimeRobot since activation for a Black Friday plan, and named praise for a support agent who walked a customer through a plan upgrade. Support quality and price come up far more often than raw performance.

A long-running third-party writeup from someone running a 4 vCPU plan in Los Angeles DC-02 for around eighteen months describes it as stable, with a real human reply to an early-hours ticket in about 20 minutes, and openly says the setup is a poor fit for sub-5ms Tokyo latency or a high-IOPS hot database. That matches what the hardware is: Xeon cores and RAID-10 SSD, not local NVMe.

## Who should not buy this

Skip RackNerd if you want managed hosting and someone else to own the stack. Skip it if your application needs single-digit-millisecond latency to East Asia, or if you're running a write-heavy production database where IOPS is the constraint and a single instance without replicas is your plan. Skip the 1 GB plan if you already know you're installing an LLM front end, and skip the 2 GB if n8n is going to carry real workflows plus a database.

Also skip the $21.99 tier if your site runs WooCommerce with Redis and a page builder on the same box. The plan is fine. The workload isn't.

## Picking one in thirty seconds

WireGuard, Webmin, a static site, a small blog: **1 GB, $21.99/year**. n8n solo, Coolify, AdminBolt, a Docker playground, a VPN with a handful of peers: **2 GB, $35.99/year**. Ollama with Open WebUI, LibreChat, AnythingLLM, Hermes Agent, or n8n in production with Postgres: **4 GB, $59.99/year**. OpenClaw, or a multi-service stack you don't want to revisit: **8 GB, $119.99/year**.

Before you pay, confirm two things at checkout: the datacenter location, which is selected during ordering and painful to change afterward, and the billing cycle, since these prices are the annual specials rather than the monthly standard line. RackNerd provisions in minutes, and the login email lands separately from the order confirmation.

👉 [Pick your RackNerd plan and datacenter](https://bit.ly/RacKnerd)
