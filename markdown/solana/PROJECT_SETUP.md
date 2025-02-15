# 💻 Requirements

You will need to [install the Solana CLI](https://docs.solana.com/cli/install-solana-cli-tools) to complete this Pathway.

## 🐑 Local clone

If you cloned the `learn-web3-dapp` repo locally, pay attention to the following:

{% hint style="tip" %}
**Windows Users:** There are known compatibility issues with the Solana BPF toolchain. You will need to use the Windows Subsystem for Linux to compile Solana programs. Please refer to the [installation guide](https://docs.figment.io/network-documentation/extra-guides/solana-setup-for-windows) we have provided.\
**macOS Users:** If you are using any Apple Silicon products (M1 processor), you may need to build the Solana CLI from source. [Refer to this article for more information](https://dev.to/codenjobs/how-to-make-solana-test-validator-work-with-a-macbook-with-m1-chip-5emd).
{% endhint %}

---

# 🧩 DataHub API keys

To make use of the Pathway content, you will require a DataHub account and a valid API key to access Solana via DataHub's infrastructure. [Sign up for a DataHub account](https://datahub-beta.figment.io/signup) and verify your email address.

To use your API key, you must create a new file named `.env.local` in the project root directory: `/learn-web3-dapp/.env.local`, copying the contents of the existing `.env.example` file.

> Easily duplicate the file with the terminal command `cp .env.example .env.local`!

Find your unique API key on the [**DataHub Services Dashboard**](https://datahub.figment.io/). Click on the **Solana** icon in the list of available protocols, then copy your key as shown below:

![](https://raw.githubusercontent.com/figment-networks/learn-web3-dapp/main/markdown/__images__/solana/solana-setup-00.gif)

You can then paste your unique API key into `.env.local`, as the value for the environment variable `DATAHUB_SOLANA_API_KEY`. This will authenticate you and enable you to make requests to Solana via DataHub:

```yaml
# DataHub API keys
DATAHUB_AVALANCHE_API_KEY=
DATAHUB_CELO_API_KEY=
DATAHUB_NEAR_API_KEY=
DATAHUB_POLKADOT_API_KEY=
DATAHUB_POLYGON_API_KEY=
DATAHUB_SECRET_API_KEY=
DATAHUB_SOLANA_API_KEY=81436edcf907b0fbb8493d281cdff5af
DATAHUB_TEZOS_API_KEY=
```

---

# 🤖 Using a Test Validator

At some point it may be necessary to run a Test Validator. For example, if you can't get airdrops because the Devnet faucet is not working. To run a local Test Validator you will need to have the Solana CLI installed. Use this command in its own terminal tab or window :

```text
solana-test-validator
```

Use `solana config set` to target a particular cluster. After setting a cluster target, any future subcommands will send/receive information from that cluster. To target a running Test Validator with the Solana CLI :

```text
solana config set --url https://localhost:8899
```

You can see which cluster the Solana command-line tool (CLI) is currently targeting and the paths to your keypair and configuration file with the command :

```text
solana config get
```

---

# 🔐 Keypair storage

During the "Create an account" step, you will need to generate a keypair for use in the tutorials (by completing the code challenge). This keypair is kept in the localstorage of your web browser, and is distinct from any keypairs generated by the Solana CLI. After the keypair is generated, it will remain visible (and copyable) at the top of the screen.

![](https://raw.githubusercontent.com/figment-networks/learn-web3-dapp/main/markdown/__images__/solana/solana-setup-02.png)

---

# 👣 Next Steps

Once you have your Solana API key saved in `/learn-web3-dapp/.env.local`, you're ready to begin.
Click on the **Next: Connect to Solana** button below.
