## Lab Report No. 2 &mdash; Web Servers & Secure Shell

> #### *"This laboratory report's itinerary: consult the Java Runtime Environment in inaugurating a linked connection to a chat web server; generate private and public authentication tokens via `ssh` (Secure Shell) to effortlessly connect to a remote server."*

### <ins>Chat Server Program</ins>
```java
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String chatLog = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return chatLog;
        }
        else if (url.getPath().equals("/add-message")) {
                String[] args = url.getQuery().split("&");
                    String msg = args[0].substring(args[0].indexOf("=") + 1);
                    String user = args[1].substring(args[1].indexOf("=") + 1);
                    chatLog += String.format("%s: %s" + "\n", user, msg);
                    return chatLog;
                }
            
        return "404 Not Found!";
        }
    }

class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
