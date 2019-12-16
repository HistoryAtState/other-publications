# Other Publications

Source data for:

- [Foreign Relations of the United States Guide to Sources on Vietnam, 1969-1975](https://history.state.gov/historicaldocuments/guide-to-sources-on-vietnam-1969-1975)
- [Office of the Historian Frequently Asked Questions](https://history.state.gov/about/faq)
- [Homes of the Department of State, 1774-1976](https://history.state.gov/departmenthistory/buildings)
- [Short History of the Department of State](https://history.state.gov/departmenthistory/short-history)
- [U.S. Foreign Relations Materials in the Pre-1861 U.S. Congressional Serial Set](https://history.state.gov/historicaldocuments/pre-1861/serial-set)
- [Views From the Embassy: The Role of the U.S. Diplomatic Community in France, 1914](https://history.state.gov/departmenthistory/wwi)

## Build

1. Single `xar` file: The `collection.xconf` will only contain the index, not any triggers!
    ```shell
    ant
    ```

2. DEV environment: The replication triggers for the producer server are enabled in  `collection.xconf` and point to the dev server's replication service IP.
    ```shell
    ant xar-dev
    ```

3. PROD environment: Same as in 2. but for PROD destination
    ```shell
    ant xar-prod
    ```
