# Working with Temporal

This document is not meant to be a Temporal guide/tutorial. It only serves as a list of practices we must enforce as much as possible to have a consistent developer experience when working with Temporal.

### Running the codec server

All data going through Temporal is encoded. The Temporal codec server is used to decode encoded payloads. As of today, for simplicity and security reasons, it's voluntarily not deployed in staging and production environments. It's up to the developer to run it locally.

The Temporal codec server relies on the following required environment variables:

* `CROWD_TEMPORAL_ENCRYPTION_KEY_ID`: Unique identifier (name) of the encryption key to use.
* `CROWD_TEMPORAL_ENCRYPTION_KEY`: 32 length encryption key used to encode/decode data between Temporal server, workers, and clients.

Start the code server:

```bash
$ cd ./services/apps/temporal_codec_server
$ npm run dev
```

Once the codec server is up and running, you need to configure the Temporal UI. In the top-right corner, select "**Configure Codec Server"**. Select "**Use my browser setting and ignore Namespace-level setting"** and pass `http://localhost:8888` as the codec server endpoint used by your browser:

<figure><img src="../../.gitbook/assets/Screenshot 2023-11-08 at 11.22.10 (2).png" alt=""><figcaption></figcaption></figure>

You will now be able to see decoded payloads in the Temporal UI.

### Best practices

* Workflows and activities must always have only one argument (object).
* Workflows and activities must always return only one value (object).
* Always use `StartToCloseTimeout` + `ScheduleToCloseTimeout`in tandem, and avoid using `ScheduleToStartTimeout`
* Always set a heartbeat on activities that may run more than 5 seconds.
* Run an alert activity based on SLOs to alert internal teams that SLAs may soon be breached.
