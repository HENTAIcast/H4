# H44
targets = [
    { triple = "x86_64-unknown-linux-gnu" },
    { triple = "i686-unknown-linux-gnu" },
    { triple = "aarch64-unknown-linux-gnu" },
    { triple = "powerpc64le-unknown-linux-gnu" },
    { triple = "s390x-unknown-linux-gnu" },
]

[advisories]
vulnerability = "deny"
unmaintained = "warn"
yanked = "warn"
notice = "warn"
ignore = []

[licenses]
unlicensed = "deny"
copyleft = "warn"
default = "deny"
allow = [
    "Apache-2.0",
    "Apache-2.0 WITH LLVM-exception",
    "BSD-3-Clause",
    "MIT",
    "Unicode-DFS-2016",
]
deny = [
    "CC0-1.0",
]
exceptions = [
    { allow = ["MPL-2.0"], name = "option-ext", version = "*" },
]

[bans]
multiple-versions = "warn"
wildcards = "warn"
skip = [
    { name = "bitflags", version = "1" },
    { name = "idna", version = "<0.4" },
    { name = "socket2", version = "0.4" },
    { name = "syn", version = "1" },
    { name = "toml_edit", version = "0.19" },
]
