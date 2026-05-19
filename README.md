# SmokR NFT Metadata

This repo hosts metadata JSON files and SVG assets for SmokR NFTs.

## Structure

```
common/          # 30 metadata JSONs for Common tier
rare/            # 30 metadata JSONs for Rare tier
legendary/       # 30 metadata JSONs for Legendary tier
assets/          # 70 SVG image files
```

## Why This Exists

The SmokR NFT program hardcodes metadata URIs to:
```
https://raw.githubusercontent.com/smokr/metadata/main/{tier}/{design}.json
```

Without this repo, Solscan (and other explorers) get a 404 when fetching NFT metadata — so no image displays.

## How to Set Up

1. Create a new public repo at `https://github.com/smokr/metadata`
2. Push these files to the `main` branch
3. NFT images will appear on Solscan within minutes

## Quick Push

```bash
cd /data/.openclaw/workspace/projects/smokr-nft/github-metadata
git init
git remote add origin https://github.com/smokr/metadata.git
git add .
git commit -m "Initial metadata upload"
git branch -M main
git push -u origin main
```
