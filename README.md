
# LimeSoda

Thai fake news dataset in the healthcare domain consisting of curate and manually annotated 7,191 documents (only 4,141 documents contain token labels and are used as a test set of the baseline models).

Each document in the dataset is classified as fact, fake, or undefined. Moreover, we also provide token-level annotations for validating classifier decisions based on five high-level annotation tags: misleading headline, imposter, fabrication, false connection, and misleading content.

## Dataset Organization

<pre>
LimeSoda/
  -Train/
    -DataFile1
    -DataFile2
    -...
  -Test/
    -Dir/
      -DataFile1
      -DataFile2
      -...
  -README.md
</pre>

## Dataset Format

Each line in the jsonlines file contains:
- **words** - a list of tokens tokenized by PyICU 2.4.3.
- **token_labels** - a list of token labels (token-level tags)
- **label** - "Fact News", "Fake News", or "Undefined"

## Get Started

<pre>
import json
from typing import Dict, List


def read_jsonlines(file_path: str) -> List[Dict]:
    with open(file_path) as fp:
        return [json.loads(line) for line in fp.readlines()]


data = read_jsonlines(<i><b>"put your file path here"</b></i>)
</pre>

## Citation

If you find this repo useful, please cite our paper.

<pre>
--- Coming Soon ---
</pre>
