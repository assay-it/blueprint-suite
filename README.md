<p align="center">
  <img src="./blueprint.gif" height="240" />
  <h3 align="center">Blueprint: Behavior as a Code Suite</h3>
  <p align="center"><strong>A minimal quality assessment using Behavior as a Code with https://assay.it</strong></p>

  <p align="center">
  </p>
</p>

--- 


Quality assurance of serverless applications is more complex than doing it for other runtimes. Engineering teams spend twice as much time maintaining testing environments and mocks of cloud dependencies instead of building a loyal relationship with their customers, assay.it has you covered.

[**https://assay.it**](https://assay.it) is a Software as a Service for developers to perform formal proofs of quality using type safe Behavior as a Code. It automates validation of cause-and-effect in loosely coupled topologies such as serverless applications, microservices and other systems that rely on interface syntaxes and its behaviors. It emphasizes deployment and quality assessment as a key feature along the development pipelines. Continuous proofs of the quality helps to eliminate defects at earlier phases of the feature lifecycle. It impacts on engineering teams philosophy and commitments, ensuring that your microservice(s) are always in a release-ready state.


## Getting Started


1. **Sign up for [assay.it](https://assay.it)** with your GitHub developer account. Initially, the service requires only access to your public profile, public repositories and access to commit status of connected repositories. Later, you can enable quality assessments of private repositories. 

2. **Fork [assay-it/blueprint-suite](https://github.com/assay-it/blueprint-suite)** to your own GitHub account and then add to the assay.it workspace. The example implements a minimal quality assessment suite using [category pattern](https://assay.it/doc/core/category) to connect cause-and-effect (Given/When/Then) with the networking concepts (Input/Process/Output). Just write [pure functional code](https://assay.it/doc/core) instead of clicking through UI or maintaining endless XML, YAML or JSON documents.
```go
func TestOk() assay.Arrow {
  return http.Join(
    ø.GET("https://assay.it"),
    ƒ.Code(http.StatusCodeOK),
    ƒ.Header("Content-Type").Is("text/html"),
  )
}
```

3. **Launch the quality assessment** through the user interface. The service schedules the job and returns results of assessments in a few seconds. Here, a manual job trigger is used for ad-hoc and illustration purposes. [assay.it](https://assay.it) supports integration with CI/CD so that [continuous quality evaluation](https://assay.it/doc/case-study/everything-is-continuous) is a part of the development culture. 
![](https://assay.it/doc/assets/images/screen.png)

1. Sign Up to https://assay.it
2. Fork the repository to your GitHub account
3. Go To Account > Setting and Integrate your fork (sample.assay.it) with https://assay.it
4. Run the interface assessment

**Let's have a look on the content of repository**:
* [suite.go](suite.go) implements a minimal quality assessment contract of the service.
* [.assay.json](.assay.json) configuration file, it declares what suites shall be executed.


## Further Reading

Please continue to [the core](https://assay.it/doc/core) sections for details about Behavior as a Code development and see [our advanced example on GitHub](https://github.com/assay-it/example.assay.it).

## Issues

If you experience any issues with this example, please let us know via [GitHub issues](https://github.com/assay-it/sample.assay.it/issues). We appreciate detailed and accurate reports that help us to identity, replicate the issue and advise your with the solution.


## License

[![See LICENSE](https://img.shields.io/github/license/assay-it/sample.assay.it.svg?style=for-the-badge)](LICENSE)
