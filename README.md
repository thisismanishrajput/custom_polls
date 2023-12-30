# Custom Polls


[GitHub](https://github.com/thisismanishrajput/custom_polls)

## ScreenShots

| Voting | Not Voted Yet | Voted |
| ------------- | ------------- | ------------- |
| <image width="200" src="https://github.com/thisismanishrajput/custom_polls/blob/main/assets/3.gif"> | <image width="200" src="https://github.com/thisismanishrajput/custom_polls/blob/main/assets/2.jpeg"> | <image width="200" src="https://github.com/thisismanishrajput/custom_polls/blob/main/assets/2.jpeg"> |


## Usage

Basic:

```dart
import 'package:custom_polls/custom_polls.dart';
```

```dart
Polls(
    children: [
        // This cannot be less than 2, else will throw an exception
        Polls.options(title: 'Cairo', value: option1),
        Polls.options(title: 'Mecca', value: option2),
        Polls.options(title: 'Denmark', value: option3),
        Polls.options(title: 'Mogadishu', value: option4),
        ],
        question: Text('What is the capital of Egypt'),
        currentUser: this.user,
        creatorID: this.creator,
        voteData: usersWhoVoted,
        userChoice: usersWhoVoted[this.user],
        onVoteBackgroundColor: Colors.blue,
        leadingBackgroundColor: Colors.blue,
        backgroundColor: Colors.white,
        onVote: (choice) {

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
    },
);
```

### Poll View type

```dart
Polls(
  viewType: PollsType.creator
);
```

```dart
Polls(
viewType: PollsType.voter
);
```


```dart
Polls(
viewType: PollsType.readOnly
);
```


## Why I made this plugin

The creation of this Custom Polls package was motivated by the discontinuation of the previous "polls" package, which was no longer actively maintained. Recognizing the importance of having a reliable and up-to-date polling solution for Flutter applications, I decided to fork the existing codebase and build upon it to provide a more stable and feature-rich alternative.

### kindly follow on github
[github](https://github.com/thisismanishrajput)

## You can follow me on
[twitter](https://x.com/thisisbabusaheb)
[linkedin](https://www.linkedin.com/in/thisismanishrajput)