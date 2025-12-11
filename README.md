# Moony Deployment Test

[![Moony](https://img.shields.io/badge/Moony-Deployment%20Test-blue)](https://moonylabs.com)
[![Go](https://img.shields.io/badge/Go-1.21+-00ADD8?logo=go)](https://go.dev/)
[![License](https://img.shields.io/badge/license-MIT-lightgrey.svg?style=flat)](LICENSE.md)

This repository is a live mirror of the [Open Code Protocol (OCP) server](https://github.com/code-payments/ocp-server) maintained by [Moony Labs](https://moonylabs.com) for testing and deploying Moony's infrastructure.

## About Moony

[Moony](https://moonylabs.com) is a decentralized digital asset deployed on the Solana blockchain, designed to facilitate permissionless transactions without intermediaries. All issuance is governed by an immutable smart contract that eliminates discretionary control and enables open participation in internet capital markets.

**Learn more:** [Documentation](https://moonylabs.com/docs) | [Website](https://moonylabs.com)

## Repository Purpose

This repository serves as a deployment mirror of the OCP server codebase, specifically configured for testing Moony's deployment infrastructure. The codebase is synced from the upstream [code-payments/ocp-server](https://github.com/code-payments/ocp-server) repository to ensure Moony's deployment uses the latest stable OCP server implementation.

**Note:** This repository is currently configured for testing using "Jeffy" addresses. Production deployments will use the official Moony contract addresses.

## What is the Open Code Protocol?

The Open Code Protocol (OCP) is a next-generation currency launchpad and payment system built on Solana. It provides the first L2 solution on top of Solana, utilizing an intent-based system backed by a sequencer to handle transactions.

The OCP server is a monolith containing gRPC/web services and workers that power currency deployment, payment processing, and transaction sequencing.

## Quick Start

1. **Install Go.** See the [official documentation](https://go.dev/doc/install).

2. **Clone this repository:**

```bash
git clone https://github.com/moonylabs/moony-deployment-test.git
cd moony-deployment-test
```

3. **Run the test suite:**

```bash
make test
```

## Project Structure

The implementations powering the Open Code Protocol (Intent System, Sequencer, etc) can be found in the `ocp/` package. All other packages are generic libraries and utilities.

To begin diving into core systems, we recommend starting with the following packages:
- `ocp/rpc/`: gRPC and web service implementations
- `ocp/worker/`: Backend workers that perform tasks outside of RPC and web calls

## APIs

The gRPC APIs provided by the Open Code Protocol server can be found in the [ocp-protobuf-api](https://github.com/code-payments/ocp-protobuf-api) project.

## Contributing

This repository mirrors the upstream OCP server. For contributions to the core OCP server codebase, please contribute to the [upstream repository](https://github.com/code-payments/ocp-server).

For Moony-specific deployment configurations or documentation, contributions are welcome through pull requests.

## Upstream

This repository is synced from the upstream [code-payments/ocp-server](https://github.com/code-payments/ocp-server) repository. The commit history reflects the upstream development, ensuring Moony's deployment infrastructure stays current with the latest OCP server improvements.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

---

**Moony Labs** | [Website](https://moonylabs.com) | [Documentation](https://moonylabs.com/docs) | [GitHub](https://github.com/moonylabs)
