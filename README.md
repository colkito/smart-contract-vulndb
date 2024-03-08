[<img width="700" alt="The Creed Rebellion!" src="https://user-images.githubusercontent.com/2865694/233321738-92a9335c-d331-441e-89c3-cfecb8291f01.png">](https://thecreed.xyz/)<br>
[[  🌐  ](https://thecreed.xyz/)[  🫂  ](https://community.thecreed.xyz/c/start-here)]
</sup><br/><br/>



# Smart Contract VulnDB

An open dataset of publicly available smart contract issues aggregated from various audit reports. The dataset can be accessed at 🌻 [vulns.json](dataset/vulns.json), is updated once a day, and a live demo is available 🌐 [here](https://tintinweb.github.io/smart-contract-vulndb/
).

<sup>
LMK if you're building cool things with this dataset and I'll list them here 😊🙏
</sup>

## 🔸 DataSet

[<img width="760" alt="image" src="https://github.com/tintinweb/smart-contract-vulndb/assets/2865694/1b33870e-4201-43c9-b967-cf82498b5b48">](https://github.com/tintinweb/smart-contract-vulndb/blob/main/dataset/vulns.json)


```typescript
const issue: Issue = {
  title: "<string:title>",
  severity: Severity.Medium,
  body: "<markdown-string:description>",
  dataSource: {
    name: "<string:path-like-report-identifier>",
    repo: "<string:git-or-http-url>",
    url: "<string:url>"
  }
};
```

* [vulns.json](dataset/vulns.json)

## 🔸 Live Demo 

[<img width="941" alt="image" src="https://github.com/tintinweb/smart-contract-vulndb/assets/2865694/bf9cdd59-d415-438c-9c9b-95b7f01d3d62">](https://tintinweb.github.io/smart-contract-vulndb/)

* [Demo](https://tintinweb.github.io/smart-contract-vulndb/)

## 🔸 Accessing the Latest Snapshot

- Shell
```
⇒  curl https://tintinweb.github.io/smart-contract-vulndb/cache/vulns.json
```

- JavaScript
```javascript
fetch('https://tintinweb.github.io/smart-contract-vulndb/cache/vulns.json')
  .then(response => response.text())
  .then(data => {
    // Process the retrieved data
    const issues = data.split('\n').filter(l => l.trim().length > 0).map(l => JSON.parse(l))
    console.log(issues);
  })
  .catch(error => {
    // Handle any errors that occurred during the request
    console.error('Error:', error);
  });
```

- [NodeJs](./examples/javascript/example.js)
- [TypeScript](./examples/typescript/example.ts)
- [Python](./examples/python/example.py)

## 🤓 For Nerds 

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## 🎓 Citation

If you are using this dataset in your research and paper, here's how you can cite this dataset: 

- APA6
```
Ortner, M. (n.d.). Smart Contract VulnDB. Retrieved from https://github.com/tintinweb/smart-contract-vulndb.
```

- LateX (Bib)
```
 @article{smart_contract_vulndb, 
          title={Smart Contract VulnDB}, 
          url={https://github.com/tintinweb/smart-contract-vulndb}, 
          author={Ortner, Martin}} 
 ```

