## Here is CLI command

```sh
 grep '"symbol": "TSLA"' transaction-log.txt | grep '"side": "sell"' | awk -F'"' '{print $4}' | while read order_id; do curl -s "https://example.com/api/$order_id" >> output.txt; done
```
####
Actually, we get 2 order_id from text file, then send 2 GET request to the endpoint. But it is just simulation URL.
