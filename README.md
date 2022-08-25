# Accept a payment with Node.js and Payment Element

Accept a one time payment with node.js and the PaymentElement. For a simpler integration path, please see PaymentLinks and Stripe Checkout.


**Installing and cloning manually**

If you do not want to use the Stripe CLI, you can manually clone and configure the sample yourself:

```sh
git clone https://github.com/cjavilla-stripe/accept-a-payment-node
```

Copy the .env.example file into a file named .env in the server folder. For example:

```sh
cp .env.example server/.env
```

You will need a Stripe account in order to run the demo. Once you set up your
account, go to the Stripe [developer
dashboard](https://stripe.com/docs/development#api-keys) to find your API keys.

```
STRIPE_PUBLISHABLE_KEY=<replace-with-your-publishable-key>
STRIPE_SECRET_KEY=<replace-with-your-secret-key>
```

`STATIC_DIR` tells the server where to the client files are located and does
not need to be modified unless you move the server files.

**2. Follow the server instructions on how to run:**

Pick the server language you want and follow the instructions in the server folder README on how to run.

For example, if you want to run the Node server:

```
cd server
npm install
npm start
```

**3. Run a webhook locally:**

Make sure to [install the CLI](https://stripe.com/docs/stripe-cli) and [link your Stripe account](https://stripe.com/docs/stripe-cli#link-account).

```sh
stripe listen --forward-to localhost:4242/webhook
```

The CLI will print a webhook secret key to the console. Set `STRIPE_WEBHOOK_SECRET` to this value in your .env file.

You should see events logged in the console where the CLI is running.

When you are ready to create a live webhook endpoint, follow our guide in the docs on [configuring a webhook endpoint in the dashboard](https://stripe.com/docs/webhooks/setup#configure-webhook-settings).

## FAQ

Q: Why did you pick these frameworks?

A: We chose the most minimal framework to convey the key Stripe calls and concepts you need to understand. These demos are meant as an educational tool that helps you roadmap how to integrate Stripe within your own system independent of the framework.

## Get support

If you found a bug or want to suggest a new [feature/use case/sample], please [file an issue](../../issues).

If you have questions, comments, or need help with code, we're here to help:

- on [Discord](https://stripe.com/go/developer-chat)
- on Twitter at [@StripeDev](https://twitter.com/StripeDev)
- on Stack Overflow at the [stripe-payments](https://stackoverflow.com/tags/stripe-payments/info) tag

Sign up to [stay updated with developer news](https://go.stripe.global/dev-digest).

## Author(s)

[@cjavilla-stripe](https://twitter.com/cjav_dev)

## Contributing

If you'd like to contribute to this sample, please check out the guidelines in [CONTRIBUTING.md](CONTRIBUTING.md)

## Code of conduct

This repository has a [code of conduct](CODE_OF_CONDUCT.md), please read it before opening an issue or a PR.
