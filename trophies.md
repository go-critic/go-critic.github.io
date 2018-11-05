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
1. [strings, bytes: avoid unnecessary function literals](https://go-review.googlesource.com/c/go/+/127756) `unlambda`

### [upspin/upspin](https://github.com/upspin/upspin)

1. [pack/internal/packtest: remove redundant parens in type conv](https://github.com/upspin/upspin/commit/1e73992b518722f8eb59d37ad70df02179063d76) `typeUnparen`

### [gobufallo/buffalo](https://github.com/gobuffalo/buffalo)

1. [internal/release,render: remove redundant func wrapping](https://github.com/gobuffalo/buffalo/pull/1211) `unlambda`
1. [buffalo/cmd: make len comparison more clear](https://github.com/gobuffalo/buffalo/pull/1212) `sloppyLen`

### [graphql-go/graphql](https://github.com/graphql-go/graphql)

1. [use type switch with var binding](https://github.com/graphql-go/graphql/pull/372) `typeSwitchVar`
1. [replace regexp.Compile with regexp.MustCompile](https://github.com/graphql-go/graphql/pull/373) `regexpMust`
1. [replace len(x)<=v with len(x)==v](https://github.com/graphql-go/graphql/pull/374) `sloppyLen`
1. [simplify single case type switches](https://github.com/graphql-go/graphql/pull/375) `singleCaseSwitch`
1. [simplify assignments with op= syntax](https://github.com/graphql-go/graphql/pull/376) `assignOp`

### [coreos/etcd](https://github.com/coreos/etcd)

1. [etcdctl/ctlv2/command: fix type switch case order](https://github.com/coreos/etcd/pull/9968) `caseOrder`
1. [etcdserver/api/v2discovery: simplify !(x == y) to x != y](https://github.com/coreos/etcd/pull/9969) `boolExprSimplify`
1. [contrib/recipes: use clientv3.NoLease instead of 0](https://github.com/coreos/etcd/pull/9970) `namedConst`

### [openshift/origin](https://github.com/openshift/origin)

1. [cmd/server: replace raw literals with named constants](https://github.com/openshift/origin/pull/20540) `namedConst`
1. [apps: replace func lits with wrapped func value](https://github.com/openshift/origin/pull/20541) `unlambda`
1. [build/controller/build: simplify bool exprs](https://github.com/openshift/origin/pull/20542) `boolExprSimplify`

### [mvdan/sh](https://github.com/mvdan/sh)

1. [interp: avoid redundant array copies](https://github.com/mvdan/sh/pull/253) `rangeExprCopy`
1. [interp,syntax: replace single case switches](https://github.com/mvdan/sh/pull/255) `singleCaseSwitch`
1. [syntax: replace if-else chains with expr switch stmt](https://github.com/mvdan/sh/pull/254) `ifElseChain`

### [securego/gosec](https://github.com/securego/gosec)

1. [replace len(x)<=0 with len(x)==0](https://github.com/securego/gosec/pull/220) `sloppyLen`
1. [fix duplicated index issue in Less method](https://github.com/securego/gosec/pull/221) `dupSubExpr`

### [go-reform/reform](https://github.com/go-reform/reform/pull/166)

1. [parse: replace 1 case switch with if](https://github.com/go-reform/reform/pull/166) `singleCaseSwitch`

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
1. [dashboard: append to proper slice](https://github.com/ethereum/go-ethereum/pull/17266) `appendAssign`
1. [all: simplify switches](https://github.com/ethereum/go-ethereum/pull/17267) `singleCaseSwitch`, `typeSwitchVar`

### [google/go-github](https://github.com/google/go-github)

1. [Remove redundant dereference of time.Time](https://github.com/google/go-github/pull/960) `underef`
2. [fix named consts](https://github.com/google/go-github/pull/962) `namedConst`

### [google/go-cloud](https://github.com/google/go-cloud)

1. [all: simplify and clarify some expressions](https://github.com/google/go-cloud/pull/260) `boolExprSimplify`, `typeSwitchVar`, `ifElseChain`, `namedConst`

### [ncw/rclone](https://github.com/ncw/rclone)

1. [all: fix go-critic linter suggestions](https://github.com/ncw/rclone/pull/2440) `undered`, `namedConst`, `unslice`, `builtinShadow`, `typeUnparen`

### [go-gitea/gitea](https://github.com/go-gitea/gitea)

1. [Remove check for negative length](https://github.com/go-gitea/gitea/pull/5120) `sloppyLen`
1. [Use named const instead of a raw string](https://github.com/go-gitea/gitea/pull/5115) `namedConst`
1. [Use type switch](https://github.com/go-gitea/gitea/pull/5122) `typeSwitchVar`
1. [Remove duplicated if bodies](https://github.com/go-gitea/gitea/pull/5121) `dupBranchBody`
1. [Make switch more clear](https://github.com/go-gitea/gitea/pull/5119) `defaultCaseOrder`
