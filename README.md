# perry

![image](https://user-images.githubusercontent.com/114177/160144856-ea453086-63cc-4c49-bb70-a4a9e6e0d302.png)

Perry is a simple Pair Programming CLI tool for distributed teams

## Installing

```sh
$ git clone git@github.com:dvinciguerra/perry.git ~/.perry
$ mkdir -p ~/.local/bin
$ ln -s ~/.local/bin/perry ~/.perry/perry
```

## Getting Started

### 1. starting a pair programming session

Run command `perry start` at project git repository

```
perry  main [!] λ ➜ perry start
Created autostash: 1e69ce5
Applied autostash.
[pair-7e66407a-5064-400f-9341-72019dcea5da d2bfce6] --wip-- [skip ci]
 1 file changed, 1 insertion(+)
remote:
remote: Create a pull request for 'pair-7e66407a-5064-400f-9341-72019dcea5da' on GitHub by visiting:
remote:      https://github.com/dvinciguerra/perry/pull/new/pair-7e66407a-5064-400f-9341-72019dcea5da
remote:
Unstaged changes after reset:
M       README.md
[2022-03-25T11:59:49-0300] INFO : Pair session WIP synced at branch pair-7e66407a-5064-400f-9341-72019dcea5da
```

### 2. saving WIP to pass pair control

Now we can save the current changes to pass the control to our pair

```sh
perry  pair-7e66407a-5064-400f-9341-72019dcea5da [!] 9s λ ➜ perry save
Created autostash: fe10ca4
Applied autostash.
[pair-7e66407a-5064-400f-9341-72019dcea5da 2a9101d] --wip-- [skip ci]
 1 file changed, 1 insertion(+)
Unstaged changes after reset:
M       README.md
[2022-03-25T12:00:58-0300] INFO : Pair session WIP synced at branch pair-7e66407a-5064-400f-9341-72019dcea5da
```

### 3. sync branch anytime to have changes in our local machine

Let's update out local copy of this branch

```
perry  pair-7e66407a-5064-400f-9341-72019dcea5da [!] 6s λ ➜ perry sync
[2022-03-25T12:03:19-0300] INFO : Local changes saved at 'pair-session-local-7e66407a-5064-400f-9341-72019dcea5da' stash
Fast-forwarded pair-7e66407a-5064-400f-9341-72019dcea5da to 2a9101d70e48ab94978008c15a8ec9b984dbe15a.
Unstaged changes after reset:
M       README.md
```

### 4. to finish our pair process we can cleanup our WIP

**Be careful, this will remove local and remote branch with all changes!!!**

```
perry  pair-7e66407a-5064-400f-9341-72019dcea5da [$!] 6s λ ➜ perry finish
M       README.md
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
Deleted branch pair-7e66407a-5064-400f-9341-72019dcea5da (was ac50b80).
To github.com:dvinciguerra/perry.git
 - [deleted]         pair-7e66407a-5064-400f-9341-72019dcea5da
[2022-03-25T12:06:48-0300] INFO : Pair session 7e66407a-5064-400f-9341-72019dcea5da are finished. Good work!
```

## Author

Daniel Vinciguerra <daniel.vinciguerra@bivee.com.br>
