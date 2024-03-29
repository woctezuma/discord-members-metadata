# Discord Members' Metadata

This repository contains metadata of all the members in a specific guild's channel on Discord.

## Metadata

Metadata consists of:
- the nickname,
- the handle,
- the bio,
- the profile picture.

Snapshots were scraped with [a Python script][discord-scraper] and uploaded to the ["Releases"][data-snapshots] section on GitHub.

## Usage

To download bios, run [`scrape_discord.ipynb`][colab-notebook-scraper].
[![Open In Colab][colab-badge]][colab-notebook-scraper]

To find issues in the image dataset, as with [`steam-DINOv2`][steam-DINOv2], run [`find_dataset_issues.ipynb`][colab-notebook-cleanvision].
[![Open In Colab][colab-badge]][colab-notebook-cleanvision]

To filter inappropriate content, run [`discord_safety_checker.ipynb`][colab-notebook].
[![Open In Colab][colab-badge]][colab-notebook]

To download avatars and apply CLIP for image retrieval based on a text or image query, run [`download_discord_avatars.ipynb`][colab-notebook-clip].
[![Open In Colab][colab-badge]][colab-notebook-clip]

## References

- [`stable-diffusion-safety-checker`][stable-diffusion-safety-checker]: a Python package to apply the Safety Checker from Stable Diffusion. 

Here are examples of automatic tools to identify inappropriate content.

Image classification:
- [`CompVis/stable-diffusion-safety-checker`][CompVis-space]
- [`Falconsai/nsfw_image_detection`][Falconsai-space]
- [`sanali209/nsfwfilter`][sanali209-space]

Text classification:
- [`unitaryai/detoxify`][detoxify-github]
  - [`original`][detoxify-original-space]
  - [`unbiased`][detoxify-unbiased-space]
  - [`multilingual`][detoxify-multilingual-space]

<!-- Definitions -->

[discord-scraper]: <https://github.com/woctezuma/DiscordScraper>
[data-snapshots]: <https://github.com/woctezuma/discord-members-metadata/releases>
[steam-DINOv2]: <https://github.com/woctezuma/steam-DINOv2#filtering-optional>

[colab-notebook-scraper]: <https://colab.research.google.com/github/woctezuma/discord-members-metadata/blob/main/scrape_discord.ipynb>
[colab-notebook-cleanvision]: <https://colab.research.google.com/github/woctezuma/discord-members-metadata/blob/main/find_dataset_issues.ipynb>
[colab-notebook]: <https://colab.research.google.com/github/woctezuma/discord-members-metadata/blob/main/discord_safety_checker.ipynb>
[colab-notebook-clip]: <https://colab.research.google.com/github/woctezuma/discord-members-metadata/blob/main/download_discord_avatars.ipynb>
[colab-badge]: <https://colab.research.google.com/assets/colab-badge.svg>

[stable-diffusion-safety-checker]: <https://github.com/woctezuma/stable-diffusion-safety-checker>

[CompVis-space]: <https://huggingface.co/CompVis/stable-diffusion-safety-checker>
[Falconsai-space]: <https://huggingface.co/Falconsai/nsfw_image_detection>
[sanali209-space]: <https://huggingface.co/sanali209/nsfwfilter>

[detoxify-github]: <https://github.com/unitaryai/detoxify>
[detoxify-original-space]: <https://huggingface.co/unitary/toxic-bert>
[detoxify-unbiased-space]: <https://huggingface.co/unitary/unbiased-toxic-roberta>
[detoxify-multilingual-space]: <https://huggingface.co/unitary/multilingual-toxic-xlm-roberta>
