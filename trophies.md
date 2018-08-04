## Trophies

Contributions are partitioned by projects.

By "contribution", we mean all of these:

1. Commit that fixes the problem
2. Reported issue (if there is no commit yet)
3. Any other form of advices that were suggested by `go-critic`

The list is sorted by priority.
If commit exist, it should be referenced instead of issue.
If issue exist, is should be referenced (as opposed of 3 where
we have no explicit issue ticket).

This page exists mostly to determine most useful checks that can trigger on real projects.
These checks are a good candidates to be included into "default" `go-critic` list.

Most projects listed here have high base code quality, so every detected issue counts.

### [golang/go](https://github.com/golang/go)

1. [net: combine append calls in reverseaddr](https://golang.org/cl/117615) `appendCombine`
1. [cmd/link/internal/ld: avoid Reloc copies in range loops](https://golang.org/cl/113636) `rangeValCopy`
1. [cmd/compile/internal/ssa: fix partsByVarOffset.Less method](https://golang.org/cl/122776) `dupSubExpr`
1. [runtime: remove redundant explicit deref in trace.go](https://golang.org/cl/122895) `underef`
1. [cmd/link/internal/sym: uncomment code for ELF cases in RelocName](https://golang.org/cl/122896) `commentedOutCode`
1. [runtime: simplify slice expression to sliced value itself](https://go-review.googlesource.com/c/go/+/123375) `unslice`
1. [html/template: use named consts instead of their values](https://go-review.googlesource.com/c/go/+/123376) `namedConst`
1. [cmd/internal/obj/arm64: simplify some bool expressions](https://go-review.googlesource.com/c/go/+/123377) `boolExprSimplify`
1. [math,net: omit explicit true tag expr in switch](https://go-review.googlesource.com/c/go/+/123378) `switchTrue`
1. [archive/tar: remore redundant parens in type expressions](https://go-review.googlesource.com/c/go/+/123379) `typeUnparen`

### [upspin/upspin](https://github.com/upspin/upspin)

1. [pack/internal/packtest: remove redundant parens in type conv](https://github.com/upspin/upspin/commit/1e73992b518722f8eb59d37ad70df02179063d76) `typeUnparen`

### [mvdan/sh](https://github.com/mvdan/sh)

1. [interp: avoid redundant array copies](https://github.com/mvdan/sh/pull/253) `rangeExprCopy`
1. [interp,syntax: replace single case switches](https://github.com/mvdan/sh/pull/255) `singleCaseSwitch`
1. [syntax: replace if-else chains with expr switch stmt](https://github.com/mvdan/sh/pull/254) `ifElseChain`

### [rumyantseva/go-zeroservice](https://github.com/rumyantseva/go-zeroservice)

1. [app.go: rename unused param to `_`](https://github.com/rumyantseva/go-zeroservice/pull/3) `unusedParam`

### [intel-go/nff-go](https://github.com/intel-go/nff-go)

1. [Modified style in merge function](https://github.com/intel-go/nff-go/pull/338) `typeSwitchVar`, `paramTypeCombine`

### [afiskon/go-elector](https://github.com/afiskon/go-elector)

1. [minor style fixes](https://github.com/afiskon/go-elector/pull/1) `ifElseChain`, `stdExpr`, `paramTypeCombine`

### [minio/minio](https://github.com/minio/minio)

1. [simplifying if-else chains to switches](https://github.com/minio/minio/pull/6208) `singleCaseSwitch`

### [ethereum/go-ethereum](https://github.com/ethereum/go-ethereum)

1. [all: avoid copying arrays in loops](https://github.com/ethereum/go-ethereum/pull/17265) `rangeExprCopy`
2. [dashboard: append to proper slice](https://github.com/ethereum/go-ethereum/pull/17266) `appendAssign`
3. [all: simplify switches](https://github.com/ethereum/go-ethereum/pull/17267) `singleCaseSwitch`, `typeSwitchVar`

### [google/go-github](https://github.com/google/go-github)

1. [Remove redundant dereference of time.Time](https://github.com/google/go-github/pull/960) `underef`
2. [fix named consts](https://github.com/google/go-github/pull/962) `namedConst`
