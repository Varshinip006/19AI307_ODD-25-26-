# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
You are developing a YouTube-like platform. Each channel can have multiple subscribers (viewers).

Whenever the channel uploads a new video, it must instantly notify all of its subscribers.

Each subscriber prints their own message like:

"[SubscriberName]: New video from [ChannelName]! Watching now..."

The channel doesn't care who the subscribers are or how many there are—it just broadcasts the update.

Student's Objective:
Implement the Observer Pattern:

Channel = Subject
Subscriber = Observer
When a video is uploaded, all subscribed users are notified.

Notifications should include channel name and video title.


## AIM:


## ALGORITHM :

1.Create an Observer interface with notify method

2.Create Subscriber class implementing Observer

3.Create Channel class with list of subscribers

4.Read channel name and create channel object

5.Read number of subscribers and add them to channel

6.Read number of videos

7.For each video, upload and notify all subscribers



## PROGRAM:
 ```

Program to implement a SOLID Principles in Java Program
Developed by: Priya Varshini P
RegisterNumber:  212224240119

import java.util.*;

interface Observer {
    void notify(String channelName, String videoTitle);
}

class Subscriber implements Observer {
    private String name;
    
    public Subscriber(String name)
    {
        this.name=name;
    }
    public void notify(String channelName,String videoTitle)
    {
        System.out.println(name + ": New video from "+channelName + "! Watch now...");
    }
}

class Channel {
    private String name;
    private List<Observer>subscribers=new ArrayList<>();
    public Channel(String name){
        this.name=name;
    }
    public void subscribe(Observer o)
    {
        subscribers.add(o);
    }
    public void uploadVideo(String title){
        System.out.println(name+ " uploaded: "+title);
        for (Observer o : subscribers){
            o.notify(name,title);
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String channelName = sc.nextLine();

        Channel channel = new Channel(channelName);

        int n = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < n; i++) {
            String sub = sc.nextLine();
            channel.subscribe(new Subscriber(sub));
        }

        int v = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < v; i++) {
            String title = sc.nextLine();
            channel.uploadVideo(title);
        }
    }
}

```



## OUTPUT:

<img width="1202" height="316" alt="image" src="https://github.com/user-attachments/assets/ab04c3a9-19c6-44d6-985b-30b84cf2b131" />



## RESULT:
The program successfully notifies all subscribers whenever a new video is uploaded by the channel.
