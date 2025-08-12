+++
title = "Updates-Sucks"
description = "A command-line tool for automating software version monitoring for DevOps engineers and system administrators."
weight = 30

[taxonomies]
tags = ["Golang", "Monitoring", "DevOps", "Versioning", "Repositories" ]

[extra]
local_image = "projects/rustysearch/doteki_logo.webp"
social_media_card = "social_cards/projects_doteki.jpg"
canonical_url = "https://alexohneander.de/projects/updates-sucks/"
add_src_to_code_block = true
+++

## That 3 AM Cold Sweat: Did I Update That Thing?

You know the feeling. It’s that gentle, peaceful moment just before you drift off to sleep. Or maybe it’s 3 AM on a Tuesday. Your mind is blissfully empty, and then, a rogue thought, fired from the darkest recesses of your subconscious, slams into your brain:

*“That server I spun up for that ‘quick test’ in Q2 2022… is it still running?”*

A cold sweat follows. What was it running? Is it patched? Is it secretly hosting the world's largest collection of pirated cat videos? You have no idea.

As a DevOps Engineer, I’m basically a professional juggler. But instead of juggling cute, fluffy balls, I’m juggling servers, containers, microservices, and the lingering ghosts of projects past. I’m spread across so many clients and internal projects that my brain has more tabs open than a web developer on a research binge.

The biggest nightmare? The *unmanaged* resources. The ones that aren’t neatly tucked into an Ansible playbook or a Terraform state file. The digital strays you adopted out of necessity and now have to feed, walk, and occasionally scrape digital chewing gum off of. Keeping track of what’s running is hard enough. Remembering what needs to be updated is a Herculean task.

### The Breaking Point

My breaking point came after a frantic afternoon spent auditing a forgotten corner of a client’s network. I found a container running a version of a service so old, its logo was probably still carved in stone. The feeling wasn't anger, it was a deep, existential sigh. There has to be a better way than relying on my own faulty, coffee-powered memory.

I complained to my rubber duck. I stared into the void. The void stared back and whispered, “Dude, just script it.”

And you know what? The void was right.

### Introducing: updates-sucks

Because let’s be honest, they do. The process of checking for them, that is.

So, I built a beautifully simple tool to scratch my own itch: **[updates-sucks](https://github.com/wellcom-rocks/updates-sucks)**.

It’s not fancy. It won’t make you a latte or file your taxes. But what it *will* do is save your sanity.

I created a dead-simple pipeline that runs once a week. It quietly scans for my digital flock and checks which resources are lagging behind, crying out for a fresh update. It then gives me a neat little nudge, a “Hey, don’t forget this thing!” report.

It’s like having a hyper-organized, slightly passive-aggressive robot assistant whose only job is to prevent me from becoming the subject of a future IT horror story.

### How It Saves Your Bacon

The beauty of `updates-sucks` is its simplicity. It’s a lightweight Go application that focuses on one thing: checking for container image updates. No bloated dashboards, no 200-page user manuals.

1. **It checks:** It looks at the resources you tell it to watch.
2. **It compares:** It sees if a newer, shinier version is available.
3. **It reports:** It lets you know what needs your attention.

That’s it. It’s the digital equivalent of putting sticky notes on everything, but the notes apply themselves automatically and don't fall off.

### Stop the Madness. Reclaim Your Sleep

If you’re a DevOps engineer, a sysadmin, or just someone who has spun up one too many “temporary” things, I invite you to check it out. Stop letting the ghosts of servers past haunt your nights.

Give **[updates-sucks](https://github.com/wellcom-rocks/updates-sucks)** a look on GitHub. Fork it, star it, use it. Let’s make that 3 AM cold sweat a thing of the past. Your sanity (and your security team) will thank you.
