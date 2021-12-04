# README

```
$ skaffold dev -d $DEFAULT_REPO
```

## Logs

skaffold v1.35.0
https://github.com/GoogleContainerTools/skaffold/tree/v1.35.0

```
DEBU[0014] Change detectednotify.Write: "/xxx/github.com/nyuta01/skaffold-devloop-demo/demo2/main.go"  subtask=-1 task=DevLoop
DEBU[0014] Change detectednotify.Write: "/xxx/github.com/nyuta01/skaffold-devloop-demo/demo2/main.go"  subtask=-1 task=DevLoop
[app] [00] demo1 - Hello world!!
[app] [00] demo2 - Hello world!!
DEBU[0015] Found dependencies for dockerfile: [{go.mod /app true 5 5} {go.sum /app true 5 5} {. /app true 8 8}]  subtask=-1 task=DevLoop
DEBU[0015] Found dependencies for dockerfile: [{go.mod /app true 5 5} {go.sum /app true 5 5} {. /app true 8 8}]  subtask=-1 task=DevLoop
INFO[0015] files modified: [/xxx/github.com/nyuta01/skaffold-devloop-demo/demo2/main.go]  subtask=-1 task=DevLoop
DEBU[0016]  devloop: build false, sync true, deploy false  subtask=-1 task=DevLoop
Syncing 1 files for gcr.io/xxx/temp/demo2:aaaf972@sha256:d06a6275f7163adc656ae4fa4b267b125a4cba16d3d50effccf7edb4fee7684b
INFO[0016] Copying files:map[/yyy/github.com/nyuta01/skaffold-devloop-demo/demo2/main.go:[/app/main.go]]togcr.io/yyy/temp/demo2:aaaf972@sha256:d06a6275f7163adc656ae4fa4b267b125a4cba16d3d50effccf7edb4fee7684b  subtask=-1 task=DevLoop
DEBU[0016] getting client config for kubeContext: `zzz`  subtask=-1 task=DevLoop
WARN[0016] Skipping deploy due to sync error:copying files: didn't sync any files  subtask=-1 task=DevLoop
Watching for changes...
```

skaffold PR version
https://github.com/nyuta01/skaffold/pull/1

```
DEBU[0033] Change detectednotify.Write: "/xxx/github.com/nyuta01/skaffold-devloop-demo/demo2/main.go"  subtask=-1 task=DevLoop
DEBU[0033] Change detectednotify.Write: "/xxx/github.com/nyuta01/skaffold-devloop-demo/demo2/main.go"  subtask=-1 task=DevLoop
DEBU[0034] Found dependencies for dockerfile: [{go.mod /app true 5 5} {go.sum /app true 5 5} {. /app true 8 8}]  subtask=-1 task=DevLoop
DEBU[0034] Found dependencies for dockerfile: [{go.mod /app true 5 5} {go.sum /app true 5 5} {. /app true 8 8}]  subtask=-1 task=DevLoop
INFO[0034] files modified: [/xxx/github.com/nyuta01/skaffold-devloop-demo/demo2/main.go]  subtask=-1 task=DevLoop
DEBU[0036]  devloop: build false, sync true, deploy false  subtask=-1 task=DevLoop
Syncing 1 files for gcr.io/yyy/temp/demo2:aaaf972-dirty@sha256:d80fc1ba3a9368eb61ebfaea38f9436da5a242345152fc691718daee7982f6a4
INFO[0036] Copying files:map[/xxx/github.com/nyuta01/skaffold-devloop-demo/demo2/main.go:[/app/main.go]]togcr.io/yyy/temp/demo2:aaaf972-dirty@sha256:d80fc1ba3a9368eb61ebfaea38f9436da5a242345152fc691718daee7982f6a4  subtask=-1 task=DevLoop
DEBU[0036] getting client config for kubeContext: `zzz`  subtask=-1 task=DevLoop
INFO[0036] Copying files:map[/xxx/github.com/nyuta01/skaffold-devloop-demo/demo2/main.go:[/app/main.go]]togcr.io/yyy/temp/demo2:aaaf972-dirty@sha256:d80fc1ba3a9368eb61ebfaea38f9436da5a242345152fc691718daee7982f6a4  subtask=-1 task=DevLoop
DEBU[0036] getting client config for kubeContext: `zzz`  subtask=-1 task=DevLoop
DEBU[0036] Running command: [kubectl --context zzz exec demo2 --namespace demo2 -c app -i -- tar xmf - -C / --no-same-owner]  subtask=-1 task=DevLoop
DEBU[0036] Command output: [], stderr: tar: Removing leading `/' from member names  subtask=-1 task=DevLoop
Watching for changes...
[app] [00] Killing service
[app] [00] ^Csignal: interrupt
[app] [00] Starting service
[app] [00] demo2 - Hello world!!
[app] [00] demo1 - Hello world!!
```