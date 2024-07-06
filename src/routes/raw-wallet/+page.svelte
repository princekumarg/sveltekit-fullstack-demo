<script lang="ts">
  import { PrivateKey } from "@bsv/sdk";
  let WIF: string;
  let address: string;
  function createKeys() {
    const prikey = PrivateKey.fromRandom();
    WIF = prikey.toWif();
    console.log("Privatekey:", WIF);
    address = prikey.toAddress();
    console.log("Address:", address);
  }
</script>

<section>
  <button
    on:click={createKeys}
    class="bg-blue-700 text-white p-2 rounded-md mx-auto"
    >Generate New Wallet keys</button
  >
  <p>Private key of Wif={WIF}</p>
  <p>Your Bitcoin Address id={address}</p>
</section>
