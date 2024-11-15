$ clef --configdir /data/clef --keystore /data/keystore setpw 0xb1b198e85e21f382e38cdf8397ac062ee5f62bfb

WARNING!

Clef is an account management tool. It may, like any software, contain bugs.

Please take care to
- backup your keystore files,
- verify that the keystore(s) can be opened with your password.

Clef is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY;
without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR
PURPOSE. See the GNU General Public License for more details.

Enter 'ok' to proceed:
> ok

Please enter a password to store for this address:
Password:
Repeat password:

Decrypt master seed of clef
Password:
INFO [12-28|18:19:39.146] Credential store updated                 set=0xB1B198e85e21F382e38cDF8397ac062Ee5F62bfB

$ curl <http://localhost:8550> \\
  -X POST \\
  -H "Content-Type: application/json" \\
  --data '{ "id": 2, "jsonrpc": "2.0", "method": "account_signTransaction", "params": [ { "from": "0xb1b198e85e21f382e38cdf8397ac062ee5f62bfb", "to": "0x3e8c911e3b473aad5f8a11294beccf7d979f8005", "gas": "0x333", "gasPrice": "0x1", "value": "0x5f5e100", "nonce": "0x1" } ] }'

{
    "jsonrpc": "2.0",
    "id": 2,
    "result": {
        "raw": "0xf8630101820333943e8c911e3b473aad5f8a11294beccf7d979f80058405f5e1008029a0916c12fb211c5649574c6092473b3f307a059a1cc79725aa5a2abcca0f87112aa04258bdd3053fa94cddc72324aef58e3b95f2eb3c3e40534d9708de066320bb28",
        "tx": {
            "type": "0x0",
            "nonce": "0x1",
            "gasPrice": "0x1",
            "maxPriorityFeePerGas": null,
            "maxFeePerGas": null,
            "gas": "0x333",
            "value": "0x5f5e100",
            "input": "0x",
            "v": "0x29",
            "r": "0x916c12fb211c5649574c6092473b3f307a059a1cc79725aa5a2abcca0f87112a",
            "s": "0x4258bdd3053fa94cddc72324aef58e3b95f2eb3c3e40534d9708de066320bb28",
            "to": "0x3e8c911e3b473aad5f8a11294beccf7d979f8005",
            "hash": "0xfa07afcb370d0faa59984b01c918859d90da6a55b38ba9e6c17150226c09fd0b"
        }
    }
}
