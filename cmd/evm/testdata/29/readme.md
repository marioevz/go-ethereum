## EIP 4788

This test contains testcases for EIP-4788. The 4788-contract is 
located at address `0x000F3df6D732807Ef1319fB7B8bB8522d0Beac02`, and this test executes a simple transaction. It also
implicitly invokes the system tx, which sets calls the contract and sets the 
storage values
```
$ dir=./testdata/29/ && go run . t8n --state.fork=Cancun  --input.alloc=$dir/alloc.json --input.txs=$dir/txs.json --input.env=$dir/env.json --output.alloc=stdout
INFO [08-15|20:07:56.335] Trie dumping started                     root=ecde45..2af8a7
INFO [08-15|20:07:56.335] Trie dumping complete                    accounts=2 elapsed="225.848µs"
INFO [08-15|20:07:56.335] Wrote file                               file=result.json
{
  "alloc": {
    "0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b": {
      "balance": "0x16345785d871db8",
      "nonce": "0x1"
    },
    "0xbeac00541d49391ed88abf392bfc1f4dea8c4143": {
      "code": "0x3373fffffffffffffffffffffffffffffffffffffffe14604d57602036146024575f5ffd5b5f35801560495762001fff810690815414603c575f5ffd5b62001fff01545f5260205ff35b5f5ffd5b62001fff42064281555f359062001fff015500",
      "storage": {
        "0x000000000000000000000000000000000000000000000000000000000000079e": "0x000000000000000000000000000000000000000000000000000000000000079e",
        "0x000000000000000000000000000000000000000000000000000000000001879e": "0x0000beac00beac00beac00beac00beac00beac00beac00beac00beac00beac00"
      },
      "balance": "0x
    }
  }
}

```
