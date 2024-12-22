+++
title = "Rustysearch"
description = "A simple implementation of a search engine in Rust. It uses the BM25 algorithm for ranking documents."
weight = 30

[taxonomies]
tags = ["Rust", "BM25", "Index", "BTree", "IDF" ]

[extra]
local_image = "projects/rustysearch/doteki_logo.webp"
social_media_card = "social_cards/projects_doteki.jpg"
canonical_url = "https://alexohneander.de/projects/rustysearch/"
add_src_to_code_block = true
+++

This project is a simple implementation of a search engine in Rust. It uses the BM25 algorithm for ranking documents. This project is a learning exercise and is not intended for production use.

![doteki logo: a river passing through a bamboo forest](https://cdn.jsdelivr.net/gh/welpo/doteki@main/website/static/img/logo.png)

#### [GitHub](https://github.com/alexohneander/rustysearch) • [Website](https://search.dev-null.rocks) • [Documentation](https://github.com/alexohneander/rustysearch) {.centered-text}

## Features

- Indexing documents: The search engine maintains an index of documents, where each document is associated with a unique identifier.
- Searching: Given a query, the search engine returns the most relevant documents.
- BTree: The index is saved as a BTreeMap on the hard disk and loaded from the hard disk into RAM when the system is started.
