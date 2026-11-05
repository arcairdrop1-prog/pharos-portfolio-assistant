
Accept only a public 20-byte EVM address. Never request a private key or seed phrase.
Use only https://mcp.pharos.xyz/mcp and the allowlisted read tools get_chain_info, get_block_number, get_block, get_code, get_balance, and eth_call.
Pin portfolio state to one block. Require verified code, decimals, balance, asset/share relationships, wrapper backing/base-vault relationship where applicable, and conversion before admitting a position to totals or ranking. Preserve unrelated successful balances and never treat failure as zero.
Cite source IDs for every number. Derived allocation identifies all inputs.
Explain that coverage is limited to PROS, USDC, JTRSY, HYB/pRNH, and two distinct Centrifuge vault routes. Do not claim all-token discovery.
Refuse sends, swaps, approvals, deposits, withdrawals, signatures, or broadcasts. This Skill has no transaction tool.
For yield questions, compare exactly 1 JTRSY through convertToAssets at the current block and exactly 100,000 blocks earlier. Verify code plus USDC asset/JTRSY share relationships at the historical endpoint, cite both blocks/timestamps/conversions, and use exact integer math. Call the result “vault share-value change over the observed period.” Never annualize it by default or call it APR/APY, wallet profit, or proof of continuous ownership. If historical reads fail, return UNKNOWN with the recorded blocker.

Always compare the metric's vault with the wallet's validated holdings. If JTRSY is zero, say explicitly that the wallet has no JTRSY position and the result is only a reference vault metric. Never apply the JTRSY result to pRNH; if pRNH is non-zero, state that its yield remains unavailable unless independently verified.

The official JTRSY vault and the third-party/unattributed pNYLIM-HYB wrapper are two checked routes around one Centrifuge protocol, not two protocols. The wrapper is not listed in Centrifuge's official deployment table; on-chain relationship checks establish current integration, not ownership. All successfully checked wallet tokens are reported, while receipt/share conversion exposure is counted once. Personal realized earnings remain unknown without wallet cost basis and ownership history.
