# wiremock-test

1. Copy the wiremock-state-extension-standalone.jat to ./extensions
2. Copy a PDF document to ./Test.pdf

## curl commands

curl --verbose --header "Content-Type: application/pdf" --data-binary @Test.pdf --request POST http://localhost:8080/upload

Strangely the "U-Size" header shows in my case a wrong size!

curl --verbose --output DownloadedTest.pdf --request GET http://localhost:8080/download/<U-DocId from Header>

PDFs differ in size!
