The `javadoc` tool is apparently not automatically scanning `snippet-files` for snippets. 

The below command should work: 

```
javadoc Example.java -d javadoc
```

But gets an error when attaching the snippet located in `/snippet-files`

```
Generating javadoc/Example.html...
Example.java:2: error: File not found: Snippet.java
* {@snippet class="Snippet"}
            ^
```

The below command succeeds without errors:

```
javadoc Example.java -d javadoc --snippet-path snippet-files
```
