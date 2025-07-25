# 0day.today Archive

This repository contains a preserved archive of exploit data originally hosted on [0day.today](https://0day.today)


## Background

0day.today was a long-running public repository of exploits and shellcode. It hosted tens of thousands of PoCs for vulnerabilities affecting a wide range of platforms.

In early 2025, 0day.today went offline. Months later it came back but is missing all of its data, effectively erasing over a decade of exploit documentation from the internet. Due to the site's use of anti-bot protection, much of its content was never cached by the Internet Archive, making recovery difficult.


## Purpose of This Archive

This repository serves as a historical preservation effort, with the goal of:

- **Preventing the permanent loss** of technical and historical information about publicly disclosed vulnerabilities
- **Supporting security researchers, educators, and defenders** who rely on older PoCs for analysis, detection, and training
- **Providing context for CVEs**, especially for those not well-documented in other databases


## Archive Structure

We've created a top level `index.json` to make it easier to (programmatically) understand what is in the archive. Single entries look like:

```json
{
    "exploit_id": 33814,
    "date": "01/15/2020",
    "category": "dos-poc",
    "platform": "android",
    "author": "Google Security Research",
    "cve": [
        "CVE-2020-0009"
    ],
    "title": "Android - ashmem Readonly Bypasses via remap_file_pages() and ASHMEM_UNPIN Exploit",
    "original_link": "https://0day.today/exploit/33814",
    "github_raw_url": "https://raw.githubusercontent.com/vulncheck-oss/0day.today.archive/main/dos-poc/33814.txt"
},
```

We then stored all the contents of each "category" (e.g. `dos-poc`) in corresponding directories. Each entry is stored as their "$(exploit_id).txt", so in the example above you'll find the full contents in dos-poc/33814.txt.
