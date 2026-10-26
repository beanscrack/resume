# Targeted SWE resume variants

Four ATS-readable, one-page LaTeX variants of Jerry Wu's October 2026 WaterlooWorks resume. This PR deliberately leaves `public/resume.pdf` unchanged.

| Variant | Target roles | Emphasis |
| --- | --- | --- |
| `Resume_BackendSWE.tex` | Backend, distributed systems, cloud engineering | Carta APIs, Kafka, PostgreSQL, AWS, Kubernetes |
| `Resume_Systems.tex` | Systems, performance, compilers, C++ | LLVM/Clang, CUDA, static arena allocator |
| `Resume_ML_Infrastructure.tex` | ML infrastructure, inference engineering | Qwen 27B CUDA runtime, PyTorch, quantization |
| `Resume_FullStackSWE.tex` | General SWE, product/full-stack | React, Next.js, FastAPI, Carta |

Build locally: `pdflatex Resume_BackendSWE.tex` (repeat per variant), using TeX Live with lmodern, microtype, enumitem, titlesec and hyperref. PDF artifacts are also supplied separately in the chat.

**LLVM provenance:** PR [#229953](https://github.com/llvm/llvm-project/pull/229953) was independently developed but closed without merging; the author of merged PR [#234793](https://github.com/llvm/llvm-project/pull/234793) explicitly credits it as parallel work. PR [#235209](https://github.com/llvm/llvm-project/pull/235209) is a separate open LLVM optimization patch as checked October 26, 2026. No merged code is misattributed.

Allocator speedups are local, single-threaded allocation microbenchmarks (not production HFT workloads); the CUDA inference throughput is one recorded development run on a 16 GB RTX 5080. Facts and statuses should be rechecked before applications.

The source resumes include the same contact information already on the public resume. Review before merging.
