# Aleo-service

./target/debug/authorize-service --network mainnet 
./target/debug/execute-service --network mainnet

Using state root: sr1wy6m4sysesfynq3khcwalclzddx84u3msr83tmy9a586qfgx8u8skqpape
Broadcast request succeeded with status: 200 OK
Broadcast request response body: "at1wyavvu8evr0fwpmvj8zharg7myz28r3hd24p4fgk9n0ctszqqupsfl4t6h"

https://aleo.info/transaction/at1wyavvu8evr0fwpmvj8zharg7myz28r3hd24p4fgk9n0ctszqqupsfl4t6h

## credits.aleo transfer_public

``` client/src/main.rs

type CurrentNetwork = snarkvm::prelude::MainnetV0;

const AUTHORIZE_URL: &str = "http://localhost:8080/authorize";
const EXECUTE_URL: &str = "http://localhost:8081/execute";

const BROADCAST_URL: &str = "https://api.explorer.provable.com/v1/mainnet/transaction/broadcast";
const STATE_ROOT_URL: &str = "https://api.explorer.provable.com/v1/mainnet/stateRoot/latest";

program_id: ProgramID::from_str("credits.aleo")?,
function_name: Identifier::from_str("transfer_public")?,

let base_fee_in_microcredits = U64::new(75_000);

