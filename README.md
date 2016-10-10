##Kele
A Ruby Gem API client that allows authorized users to access the Bloc API. Students can get their user and enrollment info, check their mentor’s availability, see their course roadmaps, and even submit their assignments through the command line. This Gem also offers the ability to read, send, and receive messages. All data is parsed and neatly formatted into JSON for easy readability.

##Getting Started
+ Add `gem kele` into your application's Gemfile and then run `bundle`
+ or run `gem install kele` from your command line.

##Usage example
Run irb and require the gem in your lib:
```
$ irb
>> require './lib/kele.rb'
=> true
>> Kele.new("jane@gmail.com", "abc123")
```


Retrieve your user info as a JSON blob:
```
kele_client.get_me
```


Retrieve your mentor availability using the mentor_id given in the previous step:
```
kele_client.get_mentor_availability(mentor_id)
```


Retrieve your roadmap and checkpoint info using the roadmap_id and checkpoint_id given previously:
```
kele_client.get_roadmap(roadmap_id)
kele_client.get_checkpoint(checkpoint_id)
```


Retrieve and create/send new messages:
```
kele_client.get_messages
kele_client.create_message(user_id, recipient_id, token, subject, message)
```


Submit checkpoints:
```
kele_client.create_submission(assignment_branch, assignment_commit_link, checkpoint_id, comment, enrollment_id)
```
