# my-series-IV-rust-elrond-blockchain-part-2

### This project is part of a series and includes a video.

See [Here](https://github.com/elicorrales/blockchain-tutorials/blob/main/README.md) for the overall document that
refers to all the series.  
  
```
rm -rf $(find . -name Cargo.lock; find . -name target);
```
```
tree
```
```
.
├── Cargo.toml
├── meta
│   ├── Cargo.toml
│   └── src
│       └── main.rs
└── src
    └── lib.rs
```
```
erdpy contract build  --no-wasm-opt
```
NOTE: if ```lib.rs``` empty, get this error:  
```
Finished dev [unoptimized + debuginfo] target(s) in 35.06s
Running `target/debug/crowdfunding-meta build --target=wasm32-unknown-unknown --release --out-dir /home/IamDeveloper/SwDevel/blockchain/rust/rust-elrond-blockchain-projects/my-first-elrond-project/my-smart-contracts/crowdfunding/output --target-dir /home/IamDeveloper/elrondsdk/default_cargo_target --no-wasm-opt`
CRITICAL:cli:No file matches pattern [*.wasm].
```
```
find . -name "*.wasm"
./output/crowdfunding.wasm
```
