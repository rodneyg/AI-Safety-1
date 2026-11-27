# T-2195 production patch

Apply [t2195.patch](t2195.patch) at the root of the original Vercel deployment source snapshot, `dpl_4jpn5TSYPQ2QJuiDLbKMZ82rvXGH`. Pull source files from the deployment Files API. Use the existing lockfile and project dependencies when applying the patch.

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

## T-10390 chat accessibility

Apply [t10390.patch](t10390.patch) after `t2203.patch`. This names the Send message button, removes the inactive information button, and increases the contrast of the avatar text.

```sh
git apply --check /path/to/t10390.patch
git apply /path/to/t10390.patch
```

## T-11044 chat draft preservation

Apply [t11044.patch](t11044.patch) after the chat accessibility patch.
Sending a message clears its text immediately. A draft typed while the demo
prepares that reply stays in the message box for the next send.

```sh
git apply --check /path/to/t11044.patch
git apply /path/to/t11044.patch
```

## T-16842 non-interactive type check

Apply [t16842.patch](t16842.patch) after the chat draft preservation patch.
The old lint script opened an ESLint setup prompt. Run `npm run typecheck`
to check TypeScript without a prompt or extra dependencies.

```sh
git apply --check /path/to/t16842.patch
git apply /path/to/t16842.patch
```


## T-994841 input validation and bias detection

Apply [t994841-input-safety.patch](t994841-input-safety.patch) to the current application source snapshot from deployment `dpl_GNd9Cm4ws1E1P9RjD5hmzu6DJhPd`, after the earlier chat patches. The patch rejects blank and over-limit messages before adding them to the transcript, shows the 2,000-character limit, and detects explicit group-ranking stereotypes with a neutral evidence-seeking rewrite.

Evidence: [UI screenshot](evidence/t994841-input-safety.png) and [headless interaction recording](evidence/t994841-input-safety.webm).

```sh
git apply --check /path/to/t994841-input-safety.patch
git apply /path/to/t994841-input-safety.patch
pnpm exec tsc --noEmit
pnpm build
```
