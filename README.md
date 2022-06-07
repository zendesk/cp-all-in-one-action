# cp-all-in-one-action

This action runs [cp-all-in-one](https://github.com/confluentinc/cp-all-in-one/tree/latest/cp-all-in-one), a Docker Compose for Confluent Platform.  See [Confluent documentation](https://docs.confluent.io/platform/current/tutorials/build-your-own-demos.html) for details.

# Usage

- `service`: up to which service in the docker-compose.yml file to run.  Default is none, so all services are run
- `github-branch-version`: which GitHub branch of [cp-all-in-one](https://github.com/confluentinc/cp-all-in-one) to run.  Default is `latest`.

Example to run ZooKeeper and broker on Confluent Platform `7.1.0`:

```yaml

    steps:

      - name: Run Confluent Platform (Confluent Server)
        uses: ./.github/actions/cp-all-in-one
        with:
          service: broker
          github-branch-version: 7.1.0-post
```

Example to run all services on `latest`:

```yaml

    steps:

      - name: Run Confluent Platform (Confluent Server)
        uses: ./.github/actions/cp-all-in-one
```
