+++
title = "Use real Servers again"
date = 2025-03-18
updated = 2025-03-18
description = "In this tutorial I will try to explain you briefly and concisely how you can set up a site-to-site VPN for the Google Cloud Network."

[taxonomies]
tags = ["baremetal", "cloud", "google", "aws", "cloud"]

[extra]
toc = false
pinned = true
quick_navigation_buttons = true
+++

![Private Cluster](https://preview.redd.it/k3pj0bjpr7s61.jpg?width=1080&crop=smart&auto=webp&s=8f1cee3bfc17c36c165e9e7dd7d5fafda6c943c6)

## The Case for Bringing Back "Real" Servers: Why the Cloud Isn't Always King

For years now, the narrative has been clear: the cloud is the future. Businesses big and small have flocked to platforms like Google Cloud and AWS, lured by promises of scalability, flexibility, and cost savings. But lately, I've been thinking: is this headlong rush to the cloud truly the best path? I believe it's time we seriously consider a return to "real" servers and acknowledge the limitations and potential pitfalls of relying solely on these tech giants.

Let's be honest, the cloud providers aren't doing anything magical. At their core, Google, Amazon, and the rest are simply running massive data centers filled with… you guessed it… servers. They've built impressive infrastructure and offer a wide range of services on top, but fundamentally, "they also just cook with water," as the saying goes. The perceived complexity and innovation can sometimes mask the underlying reality.

One of the biggest issues I've encountered, and I know many others have too, is the often-opaque pricing structure of cloud services. While the initial allure might be pay-as-you-go flexibility, the reality can be a tangled web of instance types, storage tiers, network egress fees, and a host of other charges that can quickly balloon your monthly bill. These "hidden costs" can be difficult to predict and manage, often negating the promised cost savings compared to the more predictable expenses of owning and maintaining your own hardware.

Furthermore, the increasing reliance on a handful of major cloud providers creates a significant dependency. We are essentially entrusting critical data and infrastructure to these companies, making ourselves vulnerable to their pricing changes, service outages, and even their long-term strategic decisions. This lack of control is a worrying trend, especially when considering the potential for vendor lock-in, where migrating away from a specific cloud platform becomes prohibitively expensive and complex.

Beyond the technical and economic considerations, the current political landscape adds another layer of risk to our cloud dependency. Imagine a scenario where political tensions rise, and a country like the United States, under a potential future administration, decides to impose tariffs on cloud services. Someone like Trump, for example, has shown a willingness to use tariffs as a political tool. If such tariffs were levied on cloud usage, businesses relying heavily on these platforms would face significant and potentially crippling cost increases. This geopolitical uncertainty makes the idea of having more control over our own infrastructure increasingly appealing.

In conclusion, while the cloud offers undeniable benefits in certain situations, it's crucial to have a more balanced perspective. We need to recognize that "real" servers still hold significant value, offering greater control, potentially more predictable costs, and insulation from the unpredictable nature of both cloud pricing and international politics. It's time to re-evaluate our cloud-first mentality and consider whether bringing some workloads back in-house, or at least diversifying our infrastructure, might be a more resilient and ultimately more cost-effective strategy in the long run.
