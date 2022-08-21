# my-series-IV-rust-elrond-blockchain-part-2

### This project is part of a series and includes a video.

See [Here](https://github.com/elicorrales/blockchain-tutorials/blob/main/README.md) for the overall document that
refers to all the series.  
  
> The wasm-opt program is a tool in the binaryen toolkit which is a wasm-to-wasm transformation that optimizes the input wasm module. Often wasm-opt can get 10-20% size reductions over LLVM's raw output.  
  
```
npm install -g wasm-opt
```
  
```
rm -rf $(find . -name Cargo.lock;
         find . -type d -name target;
         find . -type d -name output;
         find . -type d -name wasm);
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
