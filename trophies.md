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

### [mvdan/sh](https://github.com/mvdan/sh)

1. [interp: avoid redundant array copies](https://github.com/mvdan/sh/pull/253) `rangeExprCopy`
1. [interp,syntax: replace single case switches](https://github.com/mvdan/sh/pull/255) `singleCaseSwitch`
1. [syntax: replace if-else chains with expr switch stmt](https://github.com/mvdan/sh/pull/254) `elseif`

### [nff-go](https://github.com/intel-go/nff-go)

1. [Modified style in merge function](https://github.com/intel-go/nff-go/pull/338) `typeSwitchVar`, `paramTypeCombine`
