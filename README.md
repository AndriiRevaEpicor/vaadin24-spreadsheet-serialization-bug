# vaadin24-spreadsheet-serialization

This project reveals an issue when we want to use Session replication along with Spreadsheet

Project's skeleton was got from https://start.vaadin.com/app and used Flow/Java - Java - Maven - Spring Boot.
JDK was used as Eclipse Temurin (AdoptOpenJDK HotSpot) 21.0.3

## Issue details

When we want to use Session replication using by vaadin, kubernetes-kit and Spreadsheet then the issue will occur that
SpreadsheetHandlerImpl doesn't serializable.

Stacktrace which describe the issue will be added to the project as
well. ([non_serializable_issue_logs.txt](non_serializable_issue_logs.txt))

## Running the Application

We should to add `--add-opens java.base/java.io=ALL-UNNAMED -Dsun.io.serialization.extendedDebugInfo=true` to VM options
along with application starter to make sure that we can see serializable error messages in the logs.

After that just run the Application directly from your IDE.
