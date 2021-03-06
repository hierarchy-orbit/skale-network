# SKALE Network Product Updates (DECEMBER 2020)

These updates are posted in: 

-   <https://github.com/skalenetwork/skale-network/tree/master/updates>
-   <https://forum.skale.network/>
-   [SKALE Discord](https://discord.gg/vvUtWJB)

If you would like to suggest changes, please post, discuss, or open a GitHub issue respective of the channels listed above.

## Month focus

During December, the team was mostly focused on:

-   Fixes for schains stability, additional error handling and performance improvements
-   Skale Manager external crypto audit fixes
-   IMA: external audit fixes
-   IMA: token workflow transfer fixes and reliability enhancements
-   Skale Manager gas usage improvements for schain operations
-   Delegation workflow enhancements: undelegation requests must be completed 3 days before month end


## Code changes

December:

**SKALE Manager (1.7.1-develop.0)**
-   Improved gas usage in schains operations  [\[PR#441\]](https://github.com/skalenetwork/skale-manager/pull/441)
-   Fixed check in nodeExit functionality [\[PR#443\]](https://github.com/skalenetwork/skale-manager/pull/443)
-   Crypto audit fix: added hash on X coordinate [\[PR#445\]](https://github.com/skalenetwork/skale-manager/pull/445)
-   Updated SECURITY.md [\[PR#450\]](https://github.com/skalenetwork/skale-manager/pull/450)
-   Crypto audit fix: changed getG2 to getG2Generator and getG1 to getG1Generator [\[PR#454\]](https://github.com/skalenetwork/skale-manager/pull/454)
-   Added restriction for undelegation requests to complete before 3-day window of month end [\[PR#455\]](https://github.com/skalenetwork/skale-manager/pull/455)
-   Crypto audit: fixed range check for signature  [\[PR#456\]](https://github.com/skalenetwork/skale-manager/pull/456)
-   Added additional fixes for crypto audit  [\[PR#461\]](https://github.com/skalenetwork/skale-manager/pull/461), [\[PR#469\]](https://github.com/skalenetwork/skale-manager/pull/469)
-   Fixed modulus [\[PR#469\]](https://github.com/skalenetwork/skale-manager/pull/469)
-   Updated dependencies

**SKALE Consensus**

-   Fixed SIGILL signal right after start of skaled [\[PR#299\]](https://github.com/skalenetwork/skale-consensus/pull/299)
-   Fixed SGXWallet waiting, async sending and rebroadcasting [\[PR#300\]](https://github.com/skalenetwork/skale-consensus/pull/300), [\[PR#301\]](https://github.com/skalenetwork/skale-consensus/pull/301)
-   Fixed consensus not always completing  when SGXWallet is unstable [\[PR#302\]](https://github.com/skalenetwork/skale-consensus/pull/302)
-   Updated SECURITY.md [\[PR#303\]](https://github.com/skalenetwork/skale-consensus/pull/303)
-   Removed ECDSA public key from output[\[PR#305\]](https://github.com/skalenetwork/skale-consensus/pull/305)
-   Added log to consensus when SGX connection is reestablished[\[PR#306\]](https://github.com/skalenetwork/skale-consensus/pull/306)
-   Fixed logging for Rotating DB [\[PR#307\]](https://github.com/skalenetwork/skale-consensus/pull/307)
-   Fixed non behavior exception[\[PR#309\]](https://github.com/skalenetwork/skale-consensus/pull/309)
-   Fixed block finalization download [\[PR#310\]](https://github.com/skalenetwork/skale-consensus/pull/310)

**SGXWallet (1.66.1-develop.0)**

-   Added SGX server anti ddos protection [\[PR#247\]](https://github.com/skalenetwork/SGXWallet/pull/247), [\[PR#248\]](https://github.com/skalenetwork/SGXWallet/pull/248)
-   Added server limits check before running SGX Wallet [\[PR#249\]](https://github.com/skalenetwork/SGXWallet/pull/249), [\[PR#250\]](https://github.com/skalenetwork/SGXWallet/pull/250)
-   Fixed SGX Wallet error reporting [\[PR#251\]](https://github.com/skalenetwork/SGXWallet/pull/251)
-   Added command for getting SGX keys info [\[PR#252\]](https://github.com/skalenetwork/SGXWallet/pull/252)
-   Removed semaphore [\[PR#253\]](https://github.com/skalenetwork/SGXWallet/pull/253)
-   Updated SECURITY.md [\[PR#254\]](https://github.com/skalenetwork/SGXWallet/pull/254)
-   Fixed block mining [\[PR#256\]](https://github.com/skalenetwork/SGXWallet/pull/256)
-   Crypto Audit fix: added V2 methods to SGX Wallet [\[PR#257\]](https://github.com/skalenetwork/SGXWallet/pull/257)

**SKALED (3.2.2-develop.0)**

-   Added second verification step [\[PR#396\]](https://github.com/skalenetwork/skaled/pull/396)
-   Fixed: use consensus without ADX instructions [\[PR#397\]](https://github.com/skalenetwork/skaled/pull/397)
-   Fixed skaled not running after node restore [\[PR#398\]](https://github.com/skalenetwork/skaled/pull/398)
-   Added consensus network fixes [\[PR#399\]](https://github.com/skalenetwork/skaled/pull/399)
-   Added test case to ensure setting storage element to zero processed in skaled [\[PR#400\]](https://github.com/skalenetwork/skaled/pull/400)
-   Fixed fail verifying empty signatures [\[PR#401\]](https://github.com/skalenetwork/skaled/pull/401)
-   Fixed IMA message verification [\[PR#402\]](https://github.com/skalenetwork/skaled/pull/402)
-   Added libcurl error 52 handling consensus [\[PR#403\]](https://github.com/skalenetwork/skaled/pull/403)

**SKALE Admin (2.0.0-develop.7)**

-   Fixed IMA config generator [\[PR#355\]](https://github.com/skalenetwork/skale-admin/pull/355)
-   Fixed pycryptodome import error [\[PR#356\]](https://github.com/skalenetwork/skale-admin/pull/356)
-   Fixed failed IMA recreation [\[PR#357\]](https://github.com/skalenetwork/skale-admin/pull/357)
-   Added phantom schain checks [\[PR#358\]](https://github.com/skalenetwork/skale-admin/pull/358)
-   Moved DKG functions to skale.py [\[PR#359\]](https://github.com/skalenetwork/skale-admin/pull/359)
-   Added SGX certificates fields to sChain config [\[PR#360\]](https://github.com/skalenetwork/skale-admin/pull/360)
-   Changed default log level for skaled[\[PR#361\]](https://github.com/skalenetwork/skale-admin/pull/361)
-   Fixed phantom schains [\[PR#363\]](https://github.com/skalenetwork/skale-admin/pull/363)
-   Fixed publish pipeline [\[PR#364\]](https://github.com/skalenetwork/skale-admin/pull/364), [\[PR#365\]](https://github.com/skalenetwork/skale-admin/pull/365)
-   Made node public IP not required [\[PR#366\]](https://github.com/skalenetwork/skale-admin/pull/366)
-   Fixed IMA env [\[PR#368\]](https://github.com/skalenetwork/skale-admin/pull/368), [\[PR#369\]](https://github.com/skalenetwork/skale-admin/pull/369)
-   Enabled contracts log for IMA [\[PR#372\]](https://github.com/skalenetwork/skale-admin/pull/372)
-   Increased skaled verbosity [\[PR#375\]](https://github.com/skalenetwork/skale-admin/pull/375)
-   Added stateRoot mismatch error handling [\[PR#378\]](https://github.com/skalenetwork/skale-admin/pull/378)

**IMA (1.0.0-develop.106)**

-   Fixed generate config [\[PR#343\]](https://github.com/skalenetwork/ima/pull/343)
-   Fixed config generator script  [\[PR#344\]](https://github.com/skalenetwork/ima/pull/344)
-   Fixed schain ETH contract[\[PR#345\]](https://github.com/skalenetwork/ima/pull/345)
-   Reverted 'improve ETH refill' feature [\[PR#347\]](https://github.com/skalenetwork/ima/pull/347)
-   Added waiting for 2/3 of skaled nodes instead of all of them [\[PR#348\]](https://github.com/skalenetwork/ima/pull/348)
-   Fixed permissions for BLS binaries  [\[PR#349\]](https://github.com/skalenetwork/ima/pull/349)
-   Updated global /tmp folder usage [\[PR#350\]](https://github.com/skalenetwork/ima/pull/350)
-   Changed order of BLS common public key parts [\[PR#351\]](https://github.com/skalenetwork/ima/pull/351)
-   Adjusted contracts order in config generator [\[PR#352\]](https://github.com/skalenetwork/ima/pull/352)
-   Added SafeMath to sum the uint [\[PR#356\]](https://github.com/skalenetwork/ima/pull/356)
-   Fixed payment error [\[PR#357\]](https://github.com/skalenetwork/ima/pull/357)
-   Fixed payment on schain part [\[PR#358\]](https://github.com/skalenetwork/ima/pull/358)
-   Added skaleFeatures instance [\[PR#359\]](https://github.com/skalenetwork/ima/pull/359)
-   Fixed "transaction underpriced" error in IMA [\[PR#360\]](https://github.com/skalenetwork/ima/pull/360)
-   Added argument [\[PR#361\]](https://github.com/skalenetwork/ima/pull/361)
-   Fixed auth check prerequisites [\[PR#362\]](https://github.com/skalenetwork/ima/pull/362)
-   External audit: added adherence to best practices [\[PR#363\]](https://github.com/skalenetwork/ima/pull/363)
-   Fixed ERC20 allowance issue [\[PR#364\]](https://github.com/skalenetwork/ima/pull/364)
-   Added detailed time framing logging [\[PR#365\]](https://github.com/skalenetwork/ima/pull/365)
-   Updated code documentation [\[PR#366\]](https://github.com/skalenetwork/ima/pull/366)
-   Added transaction manager variables for the mainnet [\[PR#370\]](https://github.com/skalenetwork/ima/pull/370)
-   Fixed transaction manager issues [\[PR#374\]](https://github.com/skalenetwork/ima/pull/374), [\[PR#375\]](https://github.com/skalenetwork/ima/pull/375), [\[PR#376\]](https://github.com/skalenetwork/ima/pull/376), [\[PR#377\]](https://github.com/skalenetwork/ima/pull/377)
-   Updated logging[\[PR#378\]](https://github.com/skalenetwork/ima/pull/378), [\[PR#380\]](https://github.com/skalenetwork/ima/pull/380)
-   Fixed slither [\[PR#381\]](https://github.com/skalenetwork/ima/pull/381)
-   Improved logging [\[PR#382\]](https://github.com/skalenetwork/ima/pull/382)
-   Modified run.sh script [\[PR#383\]](https://github.com/skalenetwork/ima/pull/383)
-   Added more logging [\[PR#384\]](https://github.com/skalenetwork/ima/pull/384), [\[PR#385\]](https://github.com/skalenetwork/ima/pull/385), [\[PR#386\]](https://github.com/skalenetwork/ima/pull/386)
-   Added emit logging [\[PR#389\]](https://github.com/skalenetwork/ima/pull/389)
-   Updated dependencies

**SKALE Node CLI (2.0.0-develop.1)**

-   Updated API [\[PR#372\]](https://github.com/skalenetwork/skale-node-cli/pull/372)
-   Fixed schains DKG showing phantom schain [\[PR#375\]](https://github.com/skalenetwork/skale-node-cli/pull/375)
-   Added restore timeout [\[PR#376\]](https://github.com/skalenetwork/skale-node-cli/pull/376)
-   Added --no-tablespaces. Improved outputs [\[PR#378\]](https://github.com/skalenetwork/skale-node-cli/pull/378)
-   Add exit codes to cli commands [\[PR#388\]](https://github.com/skalenetwork/skale-node-cli/pull/388)
-   Updated dependencies

**Validator CLI (1.3.0-develop.0)**

-   Added error exit codes [\[PR#248\]](https://github.com/skalenetwork/validator-cli/pull/248)
-   Reverted accept all delegations feature [\[PR#251\]](https://github.com/skalenetwork/validator-cli/pull/251)
-   Added revert reason handler [\[PR#254\]](https://github.com/skalenetwork/validator-cli/pull/254)
-   Updated dependencies

**bounty-agent (1.1.1-develop.0)**

-   Added receipt processing exceptions handling [\[PR#100\]](https://github.com/skalenetwork/bounty-agent/pull/100)
-   Fixed set-env for publishing docker image[\[PR#101\]](https://github.com/skalenetwork/bounty-agent/pull/101)
-   Updated dependencies

**SKALE.py (5.0dev6)**

-   Fixed DEFAULT_GAS_LIMIT env [\[PR#319\]](https://github.com/skalenetwork/skale.py/pull/319)
-   Added function to send ETH with skale.wallet [\[PR#324\]](https://github.com/skalenetwork/skale.py/pull/324)
-   Removed print  [\[PR#325\]](https://github.com/skalenetwork/skale.py/pull/325)
-   Updated CODEOWNERS [\[PR#329\]](https://github.com/skalenetwork/skale.py/pull/329)
-   Added DEFAULT_GAS_PRICE env config option  [\[PR#330\]](https://github.com/skalenetwork/skale.py/pull/330)
-   Removed deprecated set-env usage  [\[PR#331\]](https://github.com/skalenetwork/skale.py/pull/331)
-   Updated dependencies

**Transaction-manager (1.1.0-develop.1)**

-   Fixed healthcheck [\[PR#139\]](https://github.com/skalenetwork/transaction-manager/pull/139)
-   Updated dependencies

**sgx.py (0.7dev2)**

-   Fixed set-env in GitHub actions publish  [\[PR#89\]](https://github.com/skalenetwork/sgx.py/pull/89)
-   Added BLS sign method  [\[PR#90\]](https://github.com/skalenetwork/sgx.py/pull/90)
-   Added V2 methods  [\[PR#92\]](https://github.com/skalenetwork/sgx.py/pull/92)
-   Updated dependencies
