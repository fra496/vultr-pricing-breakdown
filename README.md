# How Much Does Vultr Cost Per Month? The Full Pricing Breakdown by Plan Type, Region, and Workload — Plus Hidden Fees, Bandwidth Overages, and Free Credit Promos Explained (With Every Cloud Compute, Bare Metal, and GPU Tier Listed)

If you've been pricing out cloud hosting lately, you've probably noticed the same thing I did: every provider puts "$5/month" on their homepage, and every provider also wants you to read a 47-tab spreadsheet before you know what you'll actually pay. Vultr is one of those providers that does both — it advertises a $2.50/month entry point, but the moment you start clicking around, you realize there are about nine different product families, three billing models, and a handful of fees that aren't printed in the headline number.

This article is the version of the pricing page I wish I'd had when I was trying to figure out **vultr cost per month** for the first time. It pulls together every currently listed plan on the Vultr pricing page, plus the add-ons, the overage rules, the promo credits, and the catches that catch people. I'm not going to tell you Vultr is the cheapest cloud on earth — I'm going to show you what it actually costs to run each kind of workload there, and let you decide.

## Vultr Cost Per Month at a Glance

Before we get into the per-tier details, here's the cheat sheet. These are the *starting* prices for each major product family — the cheapest instance in each category. Real-world costs climb fast once you size up, but this gives you a sense of where Vultr sits in the market.

| Product Family | Cheapest Plan | What You Get | Best For |
|---|---|---|---|
| Cloud Compute (Regular, IPv6-only) | $2.50/mo | 1 vCPU, 0.5 GB RAM, 10 GB storage, 0.5 TB bandwidth | Sandboxes, testing, IPv6-native apps |
| Cloud Compute (Regular, dual-stack) | $3.50/mo | Same as above, with IPv4 | Personal blogs, low-traffic sites |
| Cloud Compute (High Performance) | $6.00/mo | 1 vCPU, 1 GB RAM, 25 GB NVMe, 2 TB bandwidth | Dev/test, small databases |
| Cloud Compute (High Frequency) | $6.00/mo | 1 vCPU, 1 GB RAM, 32 GB NVMe, 1 TB bandwidth | CMS, small game servers |
| Optimized Cloud Compute (CPU Optimized) | $28.00/mo | 1 vCPU, 2 GB RAM, 25 GB NVMe, 4 TB bandwidth | Compute-bound apps, CI/CD |
| Optimized Cloud Compute (General Purpose) | $30.00/mo | 1 vCPU, 4 GB RAM, 30 GB NVMe, 4 TB bandwidth | E-commerce, web apps, APIs |
| Optimized Cloud Compute (Memory Optimized) | $40.00/mo | 1 vCPU, 8 GB RAM, 50 GB NVMe, 5 TB bandwidth | MySQL, Memcached, real-time analytics |
| Optimized Cloud Compute (Storage Optimized) | $75.00/mo | 1 vCPU, 8 GB RAM, 150 GB NVMe, 4 TB bandwidth | Cassandra, MongoDB, OLTP |
| Bare Metal (CPU) | $120.00/mo | 4 cores/8 threads, 32 GB RAM, 480 GB SSD, 5 TB | Single-tenant dedicated servers |
| Bare Metal (GPU, L40S) | ~$0.848/GPU/hr | 8× NVIDIA L40S 48 GB, 2 TB RAM | AI inference, visual computing |
| Cloud GPU (NVIDIA H100) | $13,432/mo | 8× H100, 2 TB RAM, 32 TB NVMe | AI training, large inference |
| Block Storage | $1.00/mo | 10 GB minimum, $0.10/GB after | Extra disk for compute instances |
| Object Storage (Standard) | $18.00/mo | Includes base quota + $0.018/GB extra | S3-compatible backups, archives |
| Managed Database | $15.00/mo | Single-node starter | Hands-off MySQL/PostgreSQL/Redis |
| Kubernetes Engine (VKE) | Free control plane | You only pay for the worker nodes | Container orchestration |

The headline takeaway: **vultr cost per month** starts lower than most competitors ($2.50 vs DigitalOcean's $4 vs AWS Lightsail's $3.50), but the interesting number is the high-frequency $6 plan — that's the sweet spot where most personal projects and small businesses actually live. You can 👉 [start with that plan and grab $300 in trial credit here](https://www.vultr.com/?ref=9738262-9J).

## Cloud Compute: The Three Sub-Families Most People Don't Realize Exist

When the Vultr pricing page says "Cloud Compute starting at $2.50/month," it's compressing three different products into one number. Here's the breakdown.

### Regular Performance — the budget tier

These run on previous-generation Intel CPUs and regular (not NVMe) SSDs. They're fine for low-traffic websites, blogs, and dev sandboxes — anything where a few milliseconds of latency doesn't matter.

| Plan | vCPU | RAM | Storage | Bandwidth | Monthly |
|---|---|---|---|---|---|
| IPv6 Only (2-instance cap) | 1 | 0.5 GB | 10 GB | 0.5 TB | $2.50 |
| Starter (5-instance cap) | 1 | 0.5 GB | 10 GB | 0.5 TB | $3.50 |
| 1 / 1 GB | 1 | 1 GB | 25 GB | 1 TB | $5 |
| 1 / 2 GB | 1 | 2 GB | 55 GB | 2 TB | $10 |
| 2 / 2 GB | 2 | 2 GB | 65 GB | 3 TB | $15 |
| 2 / 4 GB | 2 | 4 GB | 80 GB | 3 TB | $20 |
| 4 / 8 GB | 4 | 8 GB | 160 GB | 4 TB | $40 |
| 6 / 16 GB | 6 | 16 GB | 320 GB | 5 TB | $80 |
| 8 / 32 GB | 8 | 32 GB | 640 GB | 6 TB | $160 |
| 16 / 64 GB | 16 | 64 GB | 1280 GB | 10 TB | $320 |
| 24 / 96 GB | 24 | 96 GB | 1600 GB | 15 TB | $640 |

The $2.50 plan is genuinely a sandbox — Vultr caps it at 2 instances per account and it's only available in their New Jersey (EWR) datacenter. If you need IPv4, the same configuration jumps to $3.50/month and is capped at 5 instances. After that, the limits disappear.

### High Performance — AMD EPYC or Intel Xeon with NVMe

This is where Vultr starts getting interesting. The hardware is current-generation, the storage is NVMe, and the bandwidth quotas are noticeably bigger than the Regular tier at the same price.

| Plan | vCPU | RAM | NVMe Storage | Bandwidth | Monthly |
|---|---|---|---|---|---|
| 1 / 1 GB | 1 | 1 GB | 25 GB | 2 TB | $6 |
| 1 / 2 GB | 1 | 2 GB | 50 GB | 3 TB | $12 |
| 2 / 2 GB | 2 | 2 GB | 60 GB | 4 TB | $18 |
| 2 / 4 GB | 2 | 4 GB | 100 GB | 5 TB | $24 |
| 4 / 8 GB | 4 | 8 GB | 180 GB | 6 TB | $48 |
| 4 / 12 GB | 4 | 12 GB | 260 GB | 7 TB | $72 |
| 8 / 16 GB | 8 | 16 GB | 350 GB | 8 TB | $96 |
| 12 / 24 GB | 12 | 24 GB | 500 GB | 12 TB | $144 |

AMD and Intel pricing is identical on Vultr — same specs, same price. Pick whichever has capacity in the region you want.

### High Frequency — 3GHz+ Intel Xeon with NVMe

These are the 3 GHz+ Xeon machines. The bandwidth is smaller than High Performance at the entry tier (1 TB vs 2 TB), but the storage is bigger and the CPU clock speed matters for things like WordPress admin panels and game servers.

| Plan | vCPU | RAM | NVMe Storage | Bandwidth | Monthly |
|---|---|---|---|---|---|
| 1 / 1 GB | 1 | 1 GB | 32 GB | 1 TB | $6 |
| 1 / 2 GB | 1 | 2 GB | 64 GB | 2 TB | $12 |
| 2 / 2 GB | 2 | 2 GB | 80 GB | 3 TB | $18 |
| 2 / 4 GB | 2 | 4 GB | 128 GB | 3 TB | $24 |
| 3 / 8 GB | 3 | 8 GB | 256 GB | 4 TB | $48 |
| 4 / 16 GB | 4 | 16 GB | 384 GB | 5 TB | $96 |
| 6 / 24 GB | 6 | 24 GB | 448 GB | 6 TB | $144 |
| 8 / 32 GB | 8 | 32 GB | 512 GB | 7 TB | $192 |
| 12 / 48 GB | 12 | 48 GB | 768 GB | 8 TB | $256 |

For most people wondering about **vultr cost per month**, the honest answer is "$6." That's the 1 vCPU / 1 GB plan in either High Performance or High Frequency, and it's the level where the platform stops feeling like a sandbox and starts feeling like a real server. You can 👉 [deploy it from the Cloud Compute page](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J).

## Optimized Cloud Compute: Dedicated vCPUs, No Noisy Neighbors

The Optimized line runs on fully dedicated AMD EPYC vCPUs — meaning your instance is the only one on those cores. The shared-tier plans above can get throttled if a neighbor is hammering the CPU; the Optimized plans can't. There are four sub-categories, each tuned to a different bottleneck.

### General Purpose — balanced CPU/RAM/storage

| Plan | vCPU | RAM | NVMe | Bandwidth | Monthly |
|---|---|---|---|---|---|
| 1 / 4 GB | 1 | 4 GB | 30 GB | 4 TB | $30 |
| 2 / 8 GB | 2 | 8 GB | 50 GB | 5 TB | $60 |
| 4 / 16 GB | 4 | 16 GB | 80 GB | 6 TB | $120 |
| 8 / 32 GB | 8 | 32 GB | 160 GB | 7 TB | $240 |
| 16 / 64 GB | 16 | 64 GB | 320 GB | 8 TB | $480 |
| 24 / 96 GB | 24 | 96 GB | 480 GB | 9 TB | $720 |
| 32 / 128 GB | 32 | 128 GB | 640 GB | 9 TB | $960 |
| 40 / 160 GB | 40 | 160 GB | 768 GB | 10 TB | $1,200 |
| 64 / 192 GB | 64 | 192 GB | 960 GB | 11 TB | $1,920 |
| 96 / 256 GB | 96 | 256 GB | 1280 GB | 12 TB | $3,840 |

### CPU Optimized — more CPU, less RAM

For video encoding, batch processing, CI/CD, HPC, ad serving, analytics.

| Plan | vCPU | RAM | NVMe | Bandwidth | Monthly |
|---|---|---|---|---|---|
| 1 / 2 GB | 1 | 2 GB | 25 GB | 4 TB | $28 |
| 2 / 4 GB (50 GB) | 2 | 4 GB | 50 GB | 5 TB | $40 |
| 2 / 4 GB (75 GB) | 2 | 4 GB | 75 GB | 5 TB | $45 |
| 4 / 8 GB (75 GB) | 4 | 8 GB | 75 GB | 6 TB | $80 |
| 4 / 8 GB (150 GB) | 4 | 8 GB | 150 GB | 6 TB | $90 |
| 8 / 16 GB (150 GB) | 8 | 16 GB | 150 GB | 7 TB | $160 |
| 8 / 16 GB (300 GB) | 8 | 16 GB | 300 GB | 7 TB | $180 |
| 16 / 32 GB (300 GB) | 16 | 32 GB | 300 GB | 8 TB | $320 |
| 16 / 32 GB (500 GB) | 16 | 32 GB | 500 GB | 8 TB | $360 |
| 32 / 64 GB (500 GB) | 32 | 64 GB | 500 GB | 9 TB | $640 |
| 32 / 64 GB (1000 GB) | 32 | 64 GB | 1000 GB | 10 TB | $720 |

### Memory Optimized — more RAM, less CPU/storage

For MySQL, Memcached, in-memory databases, real-time analytics. The RAM-to-vCPU ratio is roughly 8 GB per vCPU.

| Plan | vCPU | RAM | NVMe | Bandwidth | Monthly |
|---|---|---|---|---|---|
| 1 / 8 GB | 1 | 8 GB | 50 GB | 5 TB | $40 |
| 2 / 16 GB (100 GB) | 2 | 16 GB | 100 GB | 6 TB | $80 |
| 2 / 16 GB (200 GB) | 2 | 16 GB | 200 GB | 6 TB | $100 |
| 2 / 16 GB (400 GB) | 2 | 16 GB | 400 GB | 6 TB | $125 |
| 4 / 32 GB (200 GB) | 4 | 32 GB | 200 GB | 8 TB | $160 |
| 4 / 32 GB (400 GB) | 4 | 32 GB | 400 GB | 8 TB | $195 |
| 4 / 32 GB (800 GB) | 4 | 32 GB | 800 GB | 8 TB | $250 |
| 8 / 64 GB (400 GB) | 8 | 64 GB | 400 GB | 9 TB | $320 |
| 8 / 64 GB (800 GB) | 8 | 64 GB | 800 GB | 9 TB | $390 |
| 8 / 64 GB (1600 GB) | 8 | 64 GB | 1600 GB | 9 TB | $500 |
| 16 / 128 GB (800 GB) | 16 | 128 GB | 800 GB | 10 TB | $640 |
| 16 / 128 GB (1600 GB) | 16 | 128 GB | 1600 GB | 10 TB | $785 |
| 16 / 128 GB (3200 GB) | 16 | 128 GB | 3200 GB | 10 TB | $1,000 |
| 24 / 192 GB (1200 GB) | 24 | 192 GB | 1200 GB | 11 TB | $960 |
| 24 / 192 GB (2400 GB) | 24 | 192 GB | 2400 GB | 11 TB | $1,175 |
| 24 / 192 GB (4800 GB) | 24 | 192 GB | 4800 GB | 11 TB | $1,500 |
| 32 / 256 GB (1600 GB) | 32 | 256 GB | 1600 GB | 12 TB | $1,280 |
| 32 / 256 GB (3200 GB) | 32 | 256 GB | 3200 GB | 12 TB | $1,565 |

### Storage Optimized — heavy NVMe for big databases

For Cassandra, MongoDB, OLTP workloads. The headline is the storage: the top-end tier ships with nearly 6 TB of NVMe.

| Plan | vCPU | RAM | NVMe | Bandwidth | Monthly |
|---|---|---|---|---|---|
| 1 / 8 GB | 1 | 8 GB | 150 GB | 4 TB | $75 |
| 2 / 16 GB (320 GB) | 2 | 16 GB | 320 GB | 6 TB | $125 |
| 2 / 16 GB (480 GB) | 2 | 16 GB | 480 GB | 6 TB | $155 |
| 4 / 32 GB (640 GB) | 4 | 32 GB | 640 GB | 7 TB | $250 |
| 4 / 32 GB (960 GB) | 4 | 32 GB | 960 GB | 7 TB | $310 |
| 8 / 64 GB (1280 GB) | 8 | 64 GB | 1280 GB | 8 TB | $500 |
| 8 / 64 GB (1920 GB) | 8 | 64 GB | 1920 GB | 8 TB | $620 |
| 16 / 128 GB (2560 GB) | 16 | 128 GB | 2560 GB | 9 TB | $1,000 |
| 16 / 128 GB (3840 GB) | 16 | 128 GB | 3840 GB | 9 TB | $1,240 |
| 24 / 192 GB (3840 GB) | 24 | 192 GB | 3840 GB | 10 TB | $1,500 |
| 24 / 192 GB (5760 GB) | 24 | 192 GB | 5760 GB | 10 TB | $1,850 |
| 32 / 256 GB (5760 GB) | 32 | 256 GB | 5760 GB | 12 TB | $2,000 |

You can deploy any of these from the 👉 [Cloud Compute product page](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J).

## Bare Metal: Single-Tenant Servers With No Virtualization Layer

Vultr's Bare Metal line is fully automated — you provision a dedicated physical server through the same dashboard as a VM, billed hourly. There's a CPU-only family starting at $120/month and a GPU family starting at $0.848/GPU/hour.

### CPU Bare Metal

| Server | Cores/Threads | RAM | Storage | Bandwidth | Network | Monthly |
|---|---|---|---|---|---|---|
| Intel E3-1270 | 4c/8t @ 3.8GHz | 32 GB | 2× 240 GB SSD | 5 TB | 10 Gbps | $120 |
| Intel E-2286G | 6c/12t @ 4GHz | 32 GB | 2× 960 GB SSD | 10 TB | 10 Gbps | $185 |
| Intel E-2288G | 8c/16t @ 3.7GHz | 128 GB | 2× 1.92 TB NVMe | 10 TB | 10 Gbps | $350 |
| Intel E-2388G | 8c/16t @ 3.2GHz | 128 GB | 2× 1.92 TB NVMe | 10 TB | 10 Gbps | $350 |
| AMD EPYC 7443P | 24c/48t @ 2.85GHz | 256 GB | 2× 1.92 TB NVMe | 10 TB | 25 Gbps | $725 |
| AMD EPYC 9254 | 24c/48t @ 2.9GHz | 384 GB | 2× 1.92 TB NVMe | 10 TB | 25 Gbps | $825 |
| AMD EPYC 9354P | 64c/128t @ 3.25GHz | 768 GB | 4× 6.4 TB NVMe | 10 TB | 25 Gbps | $1,450 |
| 2× AMD EPYC 9354 | 32c/64t @ 3.2GHz | 1536 GB | 16× 6.4 TB NVMe | 10 TB | 25 Gbps | $2,925 |
| 2× AMD EPYC 7713 | 128c/256t @ 2GHz | 2048 GB | 10× 6.4 TB NVMe | 25 TB | 25 Gbps | $5,500 |

### GPU Bare Metal

GPU bare metal is billed per-GPU-per-hour, so your monthly cost depends on uptime. At the 730-hour industry-standard month, the cheapest is the 8× NVIDIA L40S server at $0.848/GPU/hr — that's roughly $4,954/month if you run it 24/7. The full lineup:

| GPU Config | GPUs | Per-GPU Hour | Est. 24/7 Monthly (730h) |
|---|---|---|---|
| 8× NVIDIA L40S 48 GB | 8 | $0.848 | ~$4,954 |
| 4× NVIDIA A100 80 GB PCIe | 4 | $1.290 | ~$3,767 |
| 8× NVIDIA HGX A100 80 GB | 8 | $1.490 | ~$8,701 |
| 8× NVIDIA HGX H100 80 GB | 8 | $2.300 | ~$13,432 |
| 1× NVIDIA GH200 (96 GB) | 1 | $2.990 | ~$2,183 |
| 8× AMD Instinct MI300X | 8 | $1.841 | ~$10,743 |

For GPU VMs (not bare metal), the GH200 cloud VM is the entry point at $2,913/month for a 36-month prepaid reserved instance, and the 8× H100 cloud VM is $13,432/month under the same reserved contract. Hourly rates for cloud GPU VMs run about 1.4× the monthly equivalent divided by 730.

## Cloud GPU Pricing Notes — Read This Before You Click "Deploy"

Vultr's GPU pricing uses a **730-hour monthly average**, billing actual calendar hours. That's different from the **672-hour cap** on standard compute, which means a GPU instance left running all month will clock ~58 more billable hours than a regular instance. If you're comparing monthly costs across providers, do the math on 730 hours, not 672.

GPU reserved instances are 36-month, 100% prepaid contracts — Vultr explicitly notes that the GH200 and H100 monthly prices above are for that contract type. Shorter commitments cost more per hour; contact sales for those. The on-demand GPU rates (when capacity is available without a contract) run substantially higher.

You can explore the full GPU lineup at the 👉 [Cloud GPU product page](https://www.vultr.com/products/cloud-gpu/?ref=9738262-9J).

## Storage, Networking, and Managed Services — The Add-On Costs

Most "vultr cost per month" calculators stop at the VM price. That's a mistake. Here's what actually shows up on the bill after the server is running.

### Block Storage

Attached disk for compute instances, billed at **$0.10/GB/month** with a 10 GB minimum ($1.00/month floor). Useful when you need more disk than the instance ships with but don't want to size up the whole VM.

### Object Storage (S3-compatible)

Two tiers, both with the same $0.018/GB overage rate:

- **Standard**: $18.00/month base, includes a base quota with extra storage at $0.018/GB.
- **Premium**: $36.00/month base, same $0.018/GB overage — higher durability/availability SLA.

Worth noting: in early 2024 Vultr roughly doubled their object-storage pricing from the old $6/TB/month. If you're shopping now based on old blog posts, you'll see higher numbers than those articles quote.

### Snapshots

**$0.05/GB/month** for stored snapshots. Pricing is subject to change, so treat this as a floor.

### DDoS Protection

**$10/month additional** per protected IP. Optional, billed separately from the instance.

### Managed Databases

Starting at **$15/month** for a single-node starter. Available for MySQL, PostgreSQL, Redis (caching), and Apache Kafka. Higher-availability clusters cost more.

### Kubernetes Engine (VKE)

The control plane is **free** — you only pay for the underlying worker VMs you deploy. By comparison, AWS EKS charges $0.10/hour (~$73/month) for the control plane, and GKE's Standard tier is similar. For teams evaluating **vultr cost per month** for a Kubernetes workload, this is one of the larger line-item savings vs the hyperscalers.

### Bandwidth Overage — the one fee that actually bites

Every instance ships with a bandwidth quota (anywhere from 0.5 TB on the IPv6 sandbox to 15 TB on big Regular Performance tiers). Go over, and you pay **$0.01/GB globally** — same rate everywhere, no per-region surprise. Inbound traffic is free.

At $0.01/GB, an extra 1 TB of outbound costs $10. An extra 10 TB costs $100. If you're running a media site or a download mirror, the bandwidth can easily exceed the instance cost itself — keep an eye on it.

## The Hidden Costs Worth Knowing About

A few things that show up on the bill but don't show up on the marketing page:

- **Bandwidth overages at $0.01/GB** are the single biggest source of unexpected charges. Set billing alerts.
- **Snapshots at $0.05/GB/month** keep accruing even after the source instance is destroyed. Delete snapshots you don't need.
- **Block and Object Storage** are billed independently of the compute instances using them. Stop the VM, keep paying for the disk.
- **Reserved IPv4 addresses** carry a small monthly fee when not attached to an instance — check the current docs for the exact rate.
- **DDoS protection at $10/month per IP** is opt-in, not opt-out. Don't enable it on IPs you don't actually need protected.
- **GPU billing uses 730 hours/month**, not the 672-hour cap on standard compute. A GPU left running all month bills more wall-clock hours than a CPU instance.
- **Promo credits expire in 30 days.** Any unused balance disappears — Vultr will start charging your card the moment the credit runs out or the 30 days pass, whichever comes first.

## Vultr Promo Codes and Free Credits for 2026

Vultr runs an aggressive new-customer credit program. Here's what's currently advertised on their official coupons page:

- **$200 free credit** — use code `FLYTWOHUNDRED` at signup
- **$250 free credit** — use code `250VULTRFLY`
- **$300 free credit** — use code `FLY300VULTR`
- **First-deposit match** — Vultr matches your first deposit dollar-for-dollar up to $100 (so deposit $100, get $200 in total credit)

All credits are valid for **30 days** and apply to new customers only. The deposit match is separate from the promo codes — you can stack a $300 code on top of a $100 deposit match for $400 in total starting credit, which is enough to run the $6 High Performance plan for free for over 60 months of compute-hours, or to burn through a GH200 GPU for about a week of pure testing.

The cleanest way to claim is to 👉 [sign up through the referral link](https://www.vultr.com/?ref=9738262-9J) — referral-signups automatically qualify for the credit program, and you can paste whichever code you want during registration. (Codes are subject to change and may be region-restricted; the official coupons page is the source of truth.)

## How Vultr Compares on Monthly Cost

I'm not going to do a full feature bake-off here — that's a different article. But on raw monthly cost for equivalent specs, here's where Vultr sits:

| Workload | Vultr | DigitalOcean | AWS Lightsail |
|---|---|---|---|
| Cheapest dual-stack VPS | $3.50 (1c/0.5GB/10GB) | $4 (1c/0.5GB/10GB) | $3.50 (1c/0.5GB/20GB) |
| 1 vCPU / 1 GB / ~25 GB NVMe | $6 (High Perf) | $6 (Basic) | $5 (Lightsail, non-NVMe) |
| 2 vCPU / 4 GB / NVMe | $24 (High Perf) | $24 (Basic) | ~$24 (Lightsail) |
| 4 vCPU / 8 GB shared | $40 (Regular Perf) | $48 (Basic) | n/a |
| 4 vCPU / 16 GB dedicated | $120 (Gen Purpose Optimized) | $96 (Premium, 4c/8GB) | n/a |
| Cheapest managed K8s control plane | Free (VKE) | Free (DOKS) | $73/mo (EKS) |
| Cheapest managed MySQL | $15 | $15 | $19.95 (RDS t3.micro) |

The pattern: Vultr is consistently a few percent cheaper than DigitalOcean on shared compute, noticeably cheaper on managed Kubernetes vs AWS, and competitive on managed databases. The biggest cost gap shows up at the dedicated-CPU tier, where Vultr's Optimized line is structured differently — you pay for a single dedicated vCPU starting at $28 (CPU Optimized) or $30 (General Purpose), versus DigitalOcean's Premium tier which starts higher but bundles more RAM per dollar.

The real differentiator isn't the headline price — it's bandwidth. Vultr's $0.01/GB overage is roughly half what the hyperscalers charge for egress, and the included quotas on High Performance plans are generous (2–12 TB depending on tier). If your app pushes a lot of outbound traffic, that gap adds up.

## Picking the Right Plan — A Quick Decision Tree

If you've read this far and still aren't sure where to land, here's a shortcut:

- **Just learning / sandbox / IPv6-native project**: $2.50/mo Regular IPv6-only. Two-instance cap is fine for one server plus a backup.
- **Personal blog or low-traffic WordPress, need IPv4**: $5/mo Regular Performance 1c/1GB, or $6/mo High Performance if you want NVMe.
- **SaaS MVP, small business site, dev environment**: $12–$24/mo High Performance. The 2 GB and 4 GB tiers cover most small workloads comfortably.
- **E-commerce, API server, production web app**: $30–$120/mo General Purpose Optimized. Dedicated vCPUs matter once real users are on it.
- **CPU-bound workloads (encoding, CI/CD, batch)**: $28–$80/mo CPU Optimized.
- **Database workloads (MySQL, Postgres, Redis)**: Memory Optimized at $40/mo for 8 GB RAM is the typical starting point.
- **Large NoSQL / heavy storage (MongoDB, Cassandra, OLTP)**: Storage Optimized at $75/mo entry.
- **Single-tenant dedicated hardware**: Bare Metal from $120/mo for the smallest Intel box.
- **AI training or large inference**: GPU Bare Metal from $0.848/GPU/hr (L40S) up to $2.990/GPU/hr (GH200). Cloud GPU VMs available for reserved contracts.

## Frequently Asked Questions

**Is the $2.50/month Vultr plan really usable?** It's IPv6-only and capped at two instances per account, currently in New Jersey only. If your app speaks IPv6 natively (most modern web apps do), it's a legitimate sandbox. If you need IPv4 — and most users hitting your site from a coffee shop still do — pay the extra dollar for the $3.50 dual-stack version.

**How is hourly billing actually calculated?** Vultr bills all servers hourly, capped at a monthly maximum. Standard compute is capped at 672 hours per month (28 days). GPU compute and some other products use a 730-hour monthly cap. The hourly rate times the monthly cap equals the monthly price — so if you run a $6/month plan for the full month, you pay $6, not $6 × (730/672).

**Does Vultr charge for ingress bandwidth?** No. Inbound traffic is free. Only outbound traffic beyond your quota is billed at $0.01/GB.

**What happens when my free credit runs out?** Vultr starts charging the payment method on file the moment the 30-day promo window expires or the credit balance hits zero — whichever comes first. There's no warning email in many cases, so set a calendar reminder.

**Can I get more than $300 in free credit?** The deposit match stacks on top of the promo codes — deposit $100 with code FLY300VULTR and you end up with $400 in starting credit. Enterprise accounts can qualify for up to $100K in cloud credits through Vultr's startup program; contact sales for that.

**Is there a contract or annual commitment?** No, on-demand compute is pay-as-you-go with no commitment. Reserved GPU instances (GH200, H100) require 36-month prepaid contracts at the advertised monthly prices. Everything else is hourly.

**Are there regional price differences?** Generally no — Vultr publishes one global price list for compute. Bandwidth overage is also a single $0.01/GB rate worldwide. The exception is the IPv6-only $2.50 plan, which is only available in New Jersey.

## The Bottom Line on Vultr Cost Per Month

After running through every tier on the pricing page, the honest summary is this: **vultr cost per month** starts at $2.50 for an IPv6 sandbox, gets real at $6 for a usable High Performance VM, gets serious at $30 for dedicated vCPU General Purpose, and scales cleanly all the way up to $5,500/month for a 128-core bare metal server or $13,432/month for an 8× H100 GPU rig. The pricing structure is unusually transparent for the industry — one global bandwidth rate, no per-region surcharges, a free Kubernetes control plane, and a 30-day credit program that lets you actually try before you commit.

What it isn't is the absolute cheapest on every spec. Hetzner beats it on raw dedicated-server pricing. Oracle's free tier is more generous. AWS and GCP have more services. But if you want a single provider that handles everything from a $6 personal blog to a GPU training cluster, with a control panel that doesn't require a certification to use, Vultr is one of the few places that scales both directions without making you switch platforms.

If you want to test any of this yourself without paying, the cleanest path is to 👉 [open an account with the referral link and apply the $300 promo code](https://www.vultr.com/?ref=9738262-9J) — that gives you 30 days to deploy a High Performance instance, a General Purpose Optimized box, a managed database, a Kubernetes cluster, or even a few hours on a GPU, and see how the bill actually looks for your workload before any of it costs you a dollar.
