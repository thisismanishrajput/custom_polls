Custom Polls
Interactive Polling for Flutter Apps

Custom Polls is a versatile package that empowers developers to seamlessly integrate interactive polls into their Flutter applications. With customizable options, real-time updates, and user-specific interactions, this package is ideal for creating engaging voting experiences within your app. Whether you're building a social platform, educational tool, or community-driven app, Flutter Polls makes it easy to add dynamic and user-friendly polls to enhance user engagement.

## Features

Customizable Polls:

Users can create and customize polls with different options.
Voting Functionality:

Users can vote on poll options.
Real-time Updates:

The UI updates in real-time to reflect the current poll results.
User Interaction:

Users can interact with the polls by selecting their preferred options.
User Authentication:

The package supports tracking votes by user, allowing for user-specific interactions.
Creator Identification:

The creator of the poll is identified.
Visual Customization:

The appearance of the polls can be customized, including background colors.

## Getting started

 

## Usage

Here is a simple example of how to use the Flutter Polls package:

```dart
import 'dart:async';
import 'package:flutter/material.dart';
import 'package:polls/polls.dart';



void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Custom Polls',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: PollView(),
    );
  }
}


class PollView extends StatefulWidget {
  @override
  _PollViewState createState() => _PollViewState();
}

class _PollViewState extends State<PollView> {

  double option1 = 1.0;
  double option2 = 0.0;
  double option3 = 1.0;
  double option4 = 1.0;
  double option5 = 1.0;
  double option6 = 3.0;
  double option7 = 2.0;
  double option8 = 1.0;

  String user = "king@mail.com";
  Map usersWhoVoted = {'sam@mail.com': 3, 'mike@mail.com' : 4, 'john@mail.com' : 1, 'kenny@mail.com' : 1};
  String creator = "eddy@mail.com";

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Container(
        child: Polls(
          children: [
            // This cannot be less than 2, else will throw an exception
            Polls.options(title: 'Cairo', value: option1),
            Polls.options(title: 'Mecca', value: option2),
            Polls.options(title: 'Denmark', value: option3),
            Polls.options(title: 'Mogadishu', value: option4),
            Polls.options(title: 'Maldives', value: option5),
            Polls.options(title: 'Brazil', value: option6),
            Polls.options(title: 'Ethiopia', value: option7),
            Polls.options(title: 'Italy', value: option8),
          ],
          question: Text('how old are you?'),
          currentUser: this.user,
          creatorID: this.creator,
          voteData: usersWhoVoted,
          userChoice: usersWhoVoted[this.user],
          onVoteBackgroundColor: Colors.blue,
          leadingBackgroundColor: Colors.blue,
          backgroundColor: Colors.white,
          onVote: (choice) {
            print(choice);
            setState(() {
              this.usersWhoVoted[this.user] = choice;
            });
            if (choice == 1) {
              setState(() {
                option1 += 1.0;
              });
            }
            if (choice == 2) {
              setState(() {
                option2 += 1.0;
              });
            }
            if (choice == 3) {
              setState(() {
                option3 += 1.0;
              });
            }
            if (choice == 4) {
              setState(() {
                option4 += 1.0;
              });
            }
            if (choice == 5) {
              setState(() {
                option5 += 1.0;
              });
            }
            if (choice == 6) {
              setState(() {
                option6 += 1.0;
              });
            }
            if (choice == 7) {
              setState(() {
                option7 += 1.0;
              });
            }
            if (choice == 8) {
              setState(() {
                option8 += 1.0;
              });
            }
          },
        ),
      ),
    );
  }
}
```

 
