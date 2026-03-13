# Javazone 2025

## How to prepare the demo ?
 + Prepare the mouse (otherwise the demo setup last more than 10 minutes)

 + Create a terminator with 3 shells splitted horizontally
 + In each shell, scroll up x9
 + In each shell, `cd ~/dev/projects/camel-quarkus-examples-upstream/data-extract-langchain4j/`
 + In shell 1, `git checkout camel-quarkus-main`
 + In shell 1, `git reset --hard 61dbc0b58ccce147f672d8d1404ada752ca1bc4`
 + In shell 1, check clean status, `git status`
 + In shell 2, `docker run --rm -it -v cqex-data-extract-ollama:/root/.ollama -p 11434:11434 --name cqex-data-extract-ollama ollama/ollama:0.9.3`
 + In shell 3, `docker exec -it cqex-data-extract-ollama ollama pull granite3.3:2b` (no big deal if it fails for the D-Day)
 + In shell 1, `mvn clean package -DskipTests`
 + In shell 1, `export QUARKUS_LANGCHAIN4J_OLLAMA_LOG_REQUESTS=true`
 + In shell 1, `java -jar target/quarkus-app/quarkus-run.jar`
 + In shell 3, prepare command `./send-conversations-to-camel-route.sh`
 + In eclipse, open `camel-quarkus-examples-upstream/data-extract-langchain4j`
    + `application.properties`
    + `CustomPojoExtractionService.java`
    + `Routes.java`
 + In eclipse, zoom in, CTRL+SHIFT+PLUS 3 times
 + In another workspace (CTRL+ALT+RIGHT), open `~/dev/projects/javazone-2025/JavaZone 2025.odp`
 + Prepare the presentation stick

## Plan

 + Intro (1 min)
 + Contexts and definitions (4 min)
 + Explanation of AI related code (6 min)
 + Explanation of Integration related code (3 min)
 + Lessons learned and next steps (4 min)
 + Conclusion (1 min)

## TODO
 + Try to repeat without network
