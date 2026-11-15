# .sync

## mesa

Mesa origin repo has a (some?) invalid object(s).

For example `feb356caff82e996ba0b898c02383fdfa3effc5f` .

- `git fsck` -> `cut -c 14-53`
- `git for-each-ref {hash}`

## omap5-sgx-ddk-um-linux (private)

The mirror is not publicly available because this repository is an unknown license.

## mediatek

```sh
curl 'https://gitlab.com/api/v4/groups/12042732/projects?include_subgroups=true' | jq '[.[] | {
  url: .http_url_to_repo,
  type: "git",
  repo: (.path_with_namespace | gsub("/"; "-"))
}]' > repos/mediatek.json
```
