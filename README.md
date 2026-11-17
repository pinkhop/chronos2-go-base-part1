# chronos2-go-base-part1

Shards 1 through 3 of the 12 that make up Amazon's [Chronos-2](https://huggingface.co/amazon/chronos-2) checkpoint, for [`chronos2-go-base`](https://github.com/pinkhop/chronos2-go-base).

Do not import this module. Import `github.com/pinkhop/chronos2-go-base`, which requires all four parts and assembles them into a ready-to-use model; `go get` fetches the parts automatically. The checkpoint is split across four modules so that each stays small enough for the Go module proxy to serve.


## Contents

| File | Bytes | SHA-256 |
|---|---|---|
| `model-00001-of-00012.safetensors` | 44,840,896 | `c85f9f35ee604a17106a65a8b9b17d00eba681a62224ebc2db786d126c689887` |
| `model-00002-of-00012.safetensors` | 44,840,912 | `c23d1e164ba2bcfb8a314bcd59bdf75b023798cd271b6cc4c11a6585926792b2` |
| `model-00003-of-00012.safetensors` | 42,481,512 | `10dd518e51094494ca844e07c04be336d356b82ec3d90d3307aa7ad3bf8c5b42` |

The shards are fp32 safetensors files cut from the upstream `model.safetensors` at revision [`29ec3766d36d6f73f0696f85560a422f50e8498c`](https://huggingface.co/amazon/chronos-2/tree/29ec3766d36d6f73f0696f85560a422f50e8498c), with every tensor bit-identical to upstream. [`weights/manifest.json`](weights/manifest.json) records the upstream source and each shard's size and SHA-256, and `make verify-weights` checks the files against it.


## Contributing

[`AGENTS.md`](AGENTS.md) describes the repository, the `make` targets, and the rules every change follows, for human and AI contributors alike.


## License

Licensed under the Apache License, Version 2.0; see [`LICENSE`](LICENSE).

Chronos-2 was created by Amazon, and its weights are distributed under Apache-2.0; see [`NOTICE`](NOTICE).
