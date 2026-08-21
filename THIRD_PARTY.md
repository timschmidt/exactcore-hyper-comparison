# Third-party dependency boundary

This repository contains only the independently written comparison harness,
tests, benchmarks, analysis scripts, and recorded reports. It does **not**
contain or redistribute exactCorelib source code.

The build consumes an external exactCorelib checkout through its public C++
headers and compiles the source files from that checkout in place. By default,
`build.rs` expects `../exactCorelib-main/trunk`; set `EXACTCORE_ROOT` to another
exactCorelib `trunk` directory when needed. exactCorelib is separately licensed
under the terms supplied by its authors. This repository's MIT/Apache-2.0
license does not relicense exactCorelib.

The Delaunay comparison uses an independently written exhaustive
empty-circumcircle implementation in `cpp/empty_circle_complex.h`. It relies on
exactCorelib only for public exact scalar types and predicates; no exactCorelib
demo source is included.

The Hyper crates are local path dependencies and are not vendored here. GMP,
MPFR, Rust crates from `Cargo.lock`, and all other external dependencies remain
subject to their respective licenses.
