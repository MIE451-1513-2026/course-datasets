# Amazon Video Games — course slice, version 1

Files for the MIE451/1513 Fall 2026 recommender-systems lab:

| File | Bytes | Contents |
|---|---:|---|
| `reviews.jsonl.gz` | 33,005,405 | 185,798 reviews from 110,804 users |
| `metadata.jsonl.gz` | 37,342,619 | Records for 39,648 parent products |
| `manifest.json` | — | Source URLs, selection rule, counts and file hashes |

Source: [Amazon Reviews 2023, McAuley Lab](https://amazon-reviews-2023.github.io/).
Credit: Hou et al., *Bridging Language and Items for Retrieval and Recommendation*
(2024), as cited by the dataset authors.

This slice copies the source records for a fixed approximately 4% sample of Video
Games reviewers and matching products. Duplicate rows, empty review text and short
histories remain for the lab's data inspection and cleaning exercises. The manifest
records the exact selection rule and hashes of both official source files.

Read the compressed JSON Lines files with Python's gzip/json modules or
`pandas.read_json(path, lines=True, convert_dates=False)`. SHA256 hashes in the
manifest identify the expected downloads. Course notebooks should use GitHub raw
URLs pinned to a commit, so future repository changes do not change the input data.

Original source conditions continue to apply. This directory does not assign a new
license to Amazon review text or product metadata. The authors discuss data licensing
[here](https://huggingface.co/datasets/McAuley-Lab/Amazon-Reviews-2023/discussions/1).
