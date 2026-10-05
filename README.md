# Sungchul Choi (최성철)

Undergraduate student in the Division of Advanced IT, Baekseok University, Korea
(B.S. in Big Data, double major in Artificial Intelligence, expected 2027.02).

I work on small language models (about 0.6B to 4B parameters) in long multi-hop question answering.
My focus is how to build the context a small model reads, without training any extra model.

### Research interests
- Small language models
- Retrieval-augmented generation and context compression
- Multi-hop question answering
- Evaluation of language models

### Research

**HOPPER: context compression for small language models**
First author, with Prof. Jin-Keun Hong. Manuscript in preparation for IJIBC.
HOPPER is a training-free sentence extraction method. It ranks sentences with BM25, expands the query once with title and capitalized words from the top-ranked sentences, and keeps the document title line of every selected sentence. Compression runs on a CPU and calls no language model.
Repository: [HOPPER](https://github.com/sungchul02/HOPPER) (code to be released after the review)

**Follow-up: where small models still fail on compressed contexts** (in progress)
Diagnostic experiments that give seven small models gold information one piece at a time (gold evidence, intermediate facts, decomposition trees) on HotpotQA, 2WikiMultihopQA and MuSiQue. So far the main cause of failure has been distracting sentences, not missing evidence.

**HOPPER-G: graph-path context construction for multi-hop QA** (in progress)
HOPPER-G replaces the one-time query expansion of HOPPER with a path search over a document graph, where document A links to document B when a sentence in A mentions the title of B. The model gets either only the sentences on the evidence path, or the path sentences plus HOPPER sentences up to the same token budget. Methods and hypotheses are fixed on development questions before held-out evaluation.
Repository: [HOPPER-G](https://github.com/sungchul02/HOPPER-G) (code to be released with the paper)

### Contact
robin0307choi@gmail.com

---

백석대학교 첨단IT학부에서 빅데이터와 인공지능을 공부하고 있습니다. 긴 다중 홉 질의응답에서 소형 언어모델이 읽을 문맥을 학습 없이 어떻게 만들지 연구하고 있습니다.

- **HOPPER**: 소형 언어모델을 위한 학습 없는 문맥 압축. 1저자, IJIBC 투고 준비 중이며 코드는 심사 후 공개합니다.
- **후속 연구 (진행 중)**: 압축된 문맥에서 소형 모델이 어디서 틀리는지 진단하고, 문서 사이의 연결을 따라 근거 경로를 골라 주는 HOPPER-G를 연구하고 있습니다. 코드는 아직 공개하지 않았습니다.
