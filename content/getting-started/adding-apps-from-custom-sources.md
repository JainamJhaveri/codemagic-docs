---
description: Add your Flutter app wherever it is hosted
title: Adding apps from custom sources
weight: 4
---

You can add apps from public or private Git-based repositories. This includes repositories requiring **SSH key authentication**. Click **Add app from custom source** on the Applications page to get started.

{{< figure size="" src="../uploads/add-app-from-custom-source1.png" caption="" >}}

Then, fill in all the required fields.

{{< figure size="" src="../uploads/add-app-from-custom-source2.png" caption="" >}}

1. Enter the Git URL for cloning the repository. The URL should be in the following format: `https://example.com/username/repo.git` or `git@example.com/username/repo.git`. 
2. If a private key is required to access the repository or any private submodules in it, upload the **SSH private key** file.
3. If the SSH key is password-protected, you'll be also asked to enter the **SSH key password**.
4. Click **Add app**.

Your app will be then listed on the Applications page and you can immediately start running builds. Note that in order to enable automatic builds, you will need to manually [set up webhooks](../building/automatic-build-triggering#webhooks).

## Repositories behind firewall

To allow Codemagic access the private repository, the following IP addresses need to be whitelisted:

1. `34.74.32.93` - used by our backend for getting basic information about the repository
2. `192.159.66.80/28` - used by our builder servers to download the code and build it
