# T-2195 production patch

Apply [t2195.patch](t2195.patch) at the root of the original Vercel deployment source snapshot, `dpl_4jpn5TSYPQ2QJuiDLbKMZ82rvXGH`. Pull source files from the deployment Files API. The original lockfile has no dependency entries. Regenerate it with the project package manager after applying the patch.

```sh
git apply --check /path/to/t2195.patch
git apply /path/to/t2195.patch
```

## T-2203 bias rewrite

Apply [t2203.patch](t2203.patch) after `t2195.patch`. **Use Alternative** fills the chat input with the suggested rewrite so the visitor can review it before sending.

```sh
git apply --check /path/to/t2203.patch
git apply /path/to/t2203.patch
```
