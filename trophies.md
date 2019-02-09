# Trophies

Contributions are partitioned by the check (diagnostic) names.

By the "contribution", we mean all of these:

1. Commit that fixes the problem
2. Reported issue (if there is no commit yet)
3. Any other form of advice that was suggested by `go-critic`

The list is sorted by priority.
If commit exist, it should be referenced instead of issue.
If issue exist, is should be referenced (as opposed of 3 where
we have no explicit issue ticket).

This page exists mostly to determine most useful checks that can trigger on real projects.
These checks are a good candidates to be included into "default" `go-critic` list.

Most projects listed here have high base code quality, so every detected issue counts.

Note that this list is not comprehensive.
It's virtually impossible to keep track of all contributions were made.

## Diagnostic

### [argOrder](https://go-critic.github.io/overview.html#argOrder-ref)

1. {**[gohugoio/hugo](https://github.com/gohugoio/hugo)**} [tpl: Fix strings.HasPrefix args order](https://github.com/gohugoio/hugo/commit/7201042946dde78d5ea4fea9cb006fb4dded55c1)
1. {**[syncthing/syncthing](https://github.com/syncthing/syncthing)**} [cmd/syncthing: Correct strings.HasPrefix args order](https://github.com/syncthing/syncthing/commit/ca47b4c218eb2e6b8aff49b58dca4dd4b65a7e10)
1. {**[etcd-io/etcd](https://github.com/etcd-io/etcd)**} [Fix strings.HasPrefix args order](https://github.com/etcd-io/etcd/commit/1fe6f109c87c4fa47775426a6a60c3b954ed5c33)
1. {**[goreleaser/goreleaser](https://github.com/goreleaser/goreleaser)**} [fix: brew strings.HasPrefix args order](https://github.com/goreleaser/goreleaser/commit/ba09765bfa2c980e3051c33c921d556a4a1b53a3)
1. {**[golang/go](https://github.com/golang/go)**} [net/rpc: fix args order in strings.Contains call](https://go-review.googlesource.com/c/go/+/161157)

### [dupSubExpr](https://go-critic.github.io/overview.html#dupSubExpr-ref)

1. {**[golang/go](https://github.com/golang/go)**} [cmd/compile/internal/ssa: fix partsByVarOffset.Less method](https://golang.org/cl/122776)
1. {**[securego/gosec](https://github.com/securego/gosec)**} [fix duplicated index issue in Less method](https://github.com/securego/gosec/pull/221)

### [caseOrder](https://go-critic.github.io/overview.html#assignOp-ref)

1. {**[coreos/etcd](https://github.com/coreos/etcd)**} [etcdctl/ctlv2/command: fix type switch case order](https://github.com/coreos/etcd/pull/9968)

### [commentedOutCode](https://go-critic.github.io/overview.html#commentedOutCode-ref)

1. {**[golang/go](https://github.com/golang/go)**} [cmd/link/internal/sym: uncomment code for ELF cases in RelocName](https://golang.org/cl/122896)
1. {**[go-kit/kit](https://github.com/go-kit/kit)**} [metrics: remove commented-out debug code](https://github.com/go-kit/kit/pull/770)
1. {**[Microsoft/DUCK](https://github.com/Microsoft/DUCK)**} [backend/ducklib: remove commentedOutCode from server.go](https://github.com/Microsoft/DUCK/pull/131)
1. {**[Microsoft/DUCK](https://github.com/Microsoft/DUCK)**} [backend/ducklib/handlers/documents: remove commented-out debug code](https://github.com/Microsoft/DUCK/pull/132)
1. {**[Microsoft/KubeGPU](https://github.com/Microsoft/KubeGPU)**} [crishim/pkg/kubeadvertise: remove commented-out code](https://github.com/Microsoft/KubeGPU/pull/39)
1. {**[future-architect/vuls](https://github.com/future-architect/vuls)**} [config: remove commented-out code from tomlloader](https://github.com/future-architect/vuls/pull/714)
1. {**[golang/dep](https://github.com/golang/dep)**} [cmd/dep,gps: remove commented-out code](https://github.com/golang/dep/pull/2030)

### [appendAssign](https://go-critic.github.io/overview.html#appendAssign-ref)

1. {**[ethereum/go-ethereum](https://github.com/ethereum/go-ethereum)**} [dashboard: append to proper slice](https://github.com/ethereum/go-ethereum/pull/17266)

### [dupBranchBody](https://go-critic.github.io/overview.html#dupBranchBody-ref)

1. {**[go-gitea/gitea](https://github.com/go-gitea/gitea)**} [Remove duplicated if bodies](https://github.com/go-gitea/gitea/pull/5121)

## Style

### [builtinShadow](https://go-critic.github.io/overview.html#builtinShadow-ref)

1. {**[ncw/rclone](https://github.com/ncw/rclone)**} [all: fix go-critic linter suggestions](https://github.com/ncw/rclone/pull/2440)
1. {**[v2ray/v2ray-core](https://github.com/v2ray/v2ray-core)**} [s/len/length/ s/cap/capacity/ to avoid builtin shadowing](https://github.com/v2ray/v2ray-core/pull/1292)

### [defaultCaseOrder](https://go-critic.github.io/overview.html#defaultCaseOrder-ref)

1. {**[go-gitea/gitea](https://github.com/go-gitea/gitea)**} [Make switch more clear](https://github.com/go-gitea/gitea/pull/5119)

### [ifElseChain](https://go-critic.github.io/overview.html#ifElseChain-ref)

1. {**[mvdan/sh](https://github.com/mvdan/sh)**} [syntax: replace if-else chains with expr switch stmt](https://github.com/mvdan/sh/pull/254)
1. {**[afiskon/go-elector](https://github.com/afiskon/go-elector)**} [minor style fixes](https://github.com/afiskon/go-elector/pull/1)
1. {**[google/go-cloud](https://github.com/google/go-cloud)**} [all: simplify and clarify some expressions](https://github.com/google/go-cloud/pull/260)
1. {**[v2ray/v2ray-core](https://github.com/v2ray/v2ray-core)**} [app/router: rewrite if-else chain to switch](https://github.com/v2ray/v2ray-core/pull/1293)
1. {**[jinzhu/gorm](https://github.com/jinzhu/gorm)**} [rewrite if-else chain as switch statement](https://github.com/jinzhu/gorm/pull/2121)

### [paramTypeCombine](https://go-critic.github.io/overview.html#paramTypeCombine-ref)

1. {**[intel-go/nff-go](https://github.com/intel-go/nff-go)**} [Modified style in merge function](https://github.com/intel-go/nff-go/pull/338)
1. {**[afiskon/go-elector](https://github.com/afiskon/go-elector)**} [minor style fixes](https://github.com/afiskon/go-elector/pull/1)

### [underef](https://go-critic.github.io/overview.html#underef-ref)

1. {**[golang/go](https://github.com/golang/go)**} [runtime: remove redundant explicit deref in trace.go](https://golang.org/cl/122895)
1. {**[google/go-github](https://github.com/google/go-github)**} [Remove redundant dereference of time.Time](https://github.com/google/go-github/pull/960)
1. {**[ncw/rclone](https://github.com/ncw/rclone)**} [all: fix go-critic linter suggestions](https://github.com/ncw/rclone/pull/2440)

### [unslice](https://go-critic.github.io/overview.html#unslice-ref)

1. {**[golang/go](https://github.com/golang/go)**} [runtime: simplify slice expression to sliced value itself](https://go-review.googlesource.com/c/go/+/123375)
1. {**[ncw/rclone](https://github.com/ncw/rclone)**} [all: fix go-critic linter suggestions](https://github.com/ncw/rclone/pull/2440)
1. {**[src-d/gitbase](https://github.com/src-d/gitbase)**} [internal/rule: simplify slice expression to sliced value itself](https://github.com/src-d/gitbase/pull/503)
1. {**[Microsoft/opengcs](https://github.com/Microsoft/opengcs)**} [service/gcsutil/gcstools: simplify slice expression to sliced value itself](https://github.com/Microsoft/opengcs/pull/260)
1. {**[future-architect/vuls](https://github.com/future-architect/vuls)**} [commands: simplify slice expression to sliced value itself](https://github.com/future-architect/vuls/pull/715)

### [boolExprSimplify](https://go-critic.github.io/overview.html#boolExprSimplify-ref)

1. {**[golang/go](https://github.com/golang/go)**} [cmd/internal/obj/arm64: simplify some bool expressions](https://go-review.googlesource.com/c/go/+/123377)
1. {**[coreos/etcd](https://github.com/coreos/etcd)**} [etcdserver/api/v2discovery: simplify !(x == y) to x != y](https://github.com/coreos/etcd/pull/9969)
1. {**[openshift/origin](https://github.com/openshift/origin)**} [build/controller/build: simplify bool exprs](https://github.com/openshift/origin/pull/20542)
1. {**[google/go-cloud](https://github.com/google/go-cloud)**} [all: simplify and clarify some expressions](https://github.com/google/go-cloud/pull/260)
1. {**[astaxie/beego](github.com/astaxie/beego)**} [all: simplify boolean expressions](https://github.com/astaxie/beego/pull/3523)
1. {**[golang/dep](https://github.com/golang/dep)**} [gps: simplify boolean expression](https://github.com/golang/dep/pull/2027)

### [switchTrue](https://go-critic.github.io/overview.html#switchTrue-ref)

1. {**[golang/go](https://github.com/golang/go)**} [math,net: omit explicit true tag expr in switch](https://go-review.googlesource.com/c/go/+/123378)
1. {**[src-d/gitbase](https://github.com/src-d/gitbase)**} [internal/rule: simplify `switch true {...}` to `switch {...}`](https://github.com/src-d/gitbase/pull/504)

### [typeUnparen](https://go-critic.github.io/overview.html#typeUnparen-ref)

1. {**[golang/go](https://github.com/golang/go)**} [archive/tar: remore redundant parens in type expressions](https://go-review.googlesource.com/c/go/+/123379)
1. {**[upspin/upspin](https://github.com/upspin/upspin)**} [pack/internal/packtest: remove redundant parens in type conv](https://github.com/upspin/upspin/commit/1e73992b518722f8eb59d37ad70df02179063d76)
1. {**[ncw/rclone](https://github.com/ncw/rclone)**} [all: fix go-critic linter suggestions](https://github.com/ncw/rclone/pull/2440)
1. {**[src-d/gitbase](https://github.com/src-d/gitbase)**} [remove redundant parenthesis](https://github.com/src-d/gitbase/pull/505)

### [unlambda](https://go-critic.github.io/overview.html#unlambda-ref)

1. {**[golang/go](https://github.com/golang/go)**} [strings, bytes: avoid unnecessary function literals](https://go-review.googlesource.com/c/go/+/127756)
1. {**[gobufallo/buffalo](https://github.com/gobuffalo/buffalo)**} [internal/release,render: remove redundant func wrapping](https://github.com/gobuffalo/buffalo/pull/1211)
1. {**[openshift/origin](https://github.com/openshift/origin)**} [apps: replace func lits with wrapped func value](https://github.com/openshift/origin/pull/20541)
1. {**[go-kit/kit](https://github.com/go-kit/kit)**} [metrics/internal/convert: use method value insetad of lambda](https://github.com/go-kit/kit/pull/767)
1. {**[golang/dep](https://github.com/golang/dep)**} [gps: replace redundand lambda wrapper with method value](https://github.com/golang/dep/pull/2029)

### [sloppyLen](https://go-critic.github.io/overview.html#sloppyLen-ref)

1. {**[gobufallo/buffalo](https://github.com/gobuffalo/buffalo)**} [buffalo/cmd: make len comparison more clear](https://github.com/gobuffalo/buffalo/pull/1212)
1. {**[graphql-go/graphql](https://github.com/graphql-go/graphql)**} [replace len(x)<=v with len(x)==v](https://github.com/graphql-go/graphql/pull/374)
1. {**[securego/gosec](https://github.com/securego/gosec)**} [replace len(x)<=0 with len(x)==0](https://github.com/securego/gosec/pull/220)
1. {**[go-gitea/gitea](https://github.com/go-gitea/gitea)**} [Remove check for negative length](https://github.com/go-gitea/gitea/pull/5120)
1. {**[go-kit/kit](https://github.com/go-kit/kit)**} [sd/lb: replace len(x)<=0 with len(x)==0](https://github.com/go-kit/kit/pull/768)
1. {**[golang/dep](https://github.com/golang/dep)**} [cmd/dep: replace `len(x)<=0` with `len(x)==0`](https://github.com/golang/dep/pull/2031)

### [typeSwitchVar](https://go-critic.github.io/overview.html#typeSwitchVar-ref)

1. {**[graphql-go/graphql](https://github.com/graphql-go/graphql)**} [use type switch with var binding](https://github.com/graphql-go/graphql/pull/372)
1. {**[intel-go/nff-go](https://github.com/intel-go/nff-go)**} [Modified style in merge function](https://github.com/intel-go/nff-go/pull/338)
1. {**[ethereum/go-ethereum](https://github.com/ethereum/go-ethereum)**} [all: simplify switches](https://github.com/ethereum/go-ethereum/pull/17267)
1. {**[google/go-cloud](https://github.com/google/go-cloud)**} [all: simplify and clarify some expressions](https://github.com/google/go-cloud/pull/260)
1. {**[go-gitea/gitea](https://github.com/go-gitea/gitea)**} [Use type switch](https://github.com/go-gitea/gitea/pull/5122)

### [regexpMust](https://go-critic.github.io/overview.html#regexpMust-ref)

1. {**[graphql-go/graphql](https://github.com/graphql-go/graphql)**} [replace regexp.Compile with regexp.MustCompile](https://github.com/graphql-go/graphql/pull/373)

### [singleCaseSwitch](https://go-critic.github.io/overview.html#regexpMust-ref)

1. {**[graphql-go/graphql](https://github.com/graphql-go/graphql)**} [simplify single case type switches](https://github.com/graphql-go/graphql/pull/375)
1. {**[mvdan/sh](https://github.com/mvdan/sh)**} [interp,syntax: replace single case switches](https://github.com/mvdan/sh/pull/255)
1. {**[go-reform/reform](https://github.com/go-reform/reform/pull/166)**} [parse: replace 1 case switch with if](https://github.com/go-reform/reform/pull/166)
1. {**[minio/minio](https://github.com/minio/minio)**} [simplifying if-else chains to switches](https://github.com/minio/minio/pull/6208)
1. {**[ethereum/go-ethereum](https://github.com/ethereum/go-ethereum)**} [all: simplify switches](https://github.com/ethereum/go-ethereum/pull/17267)
1. {**[Microsoft/KubeGPU](https://github.com/Microsoft/KubeGPU)**} [utils: replace single case type switch with if](https://github.com/Microsoft/KubeGPU/pull/38)

### [assignOp](https://go-critic.github.io/overview.html#assignOp-ref)

1. {**[graphql-go/graphql](https://github.com/graphql-go/graphql)**} [simplify assignments with op= syntax](https://github.com/graphql-go/graphql/pull/376)
1. {**[go-kit/kit](https://github.com/go-kit/kit)**} [metrics/teststat: replace `x = x <op> y` with `x <op>= y`](https://github.com/go-kit/kit/pull/769)
1. {**[Microsoft/KubeGPU](https://github.com/Microsoft/KubeGPU)**} [plugins: simplify `x = x <op> y` to `x <op>= y`](https://github.com/Microsoft/KubeGPU/pull/40)
1. {**[future-architect/vuls](https://github.com/future-architect/vuls)**} [report: simplify `x = x <op> y` to `x <op>= y`](https://github.com/future-architect/vuls/pull/716)
1. {**[golang/dep](https://github.com/golang/dep)**} [gps: simplify `x = x <op> y` to `x <op>= y`](https://github.com/golang/dep/pull/2028)

## Performance

### [appendCombine](https://go-critic.github.io/overview.html#appendCombine-ref)

1. {**[golang/go](https://github.com/golang/go)**} [net: combine append calls in reverseaddr](https://golang.org/cl/117615)

### [rangeValCopy](https://go-critic.github.io/overview.html#rangevalcopy)

1. {**[golang/go](https://github.com/golang/go)**} [cmd/link/internal/ld: avoid Reloc copies in range loops](https://golang.org/cl/113636)

### [rangeExprCopy](https://go-critic.github.io/overview.html#rangeExprCopy-ref)

1. {**[mvdan/sh](https://github.com/mvdan/sh)**} [interp: avoid redundant array copies](https://github.com/mvdan/sh/pull/253)
1. {**[ethereum/go-ethereum](https://github.com/ethereum/go-ethereum)**} [all: avoid copying arrays in loops](https://github.com/ethereum/go-ethereum/pull/17265)
