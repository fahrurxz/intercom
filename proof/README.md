# Proof Artifacts

This folder contains runtime proof for this fork's Intercom app.

## Files
- `run.log`: output from `pear run` startup and live sidechannel activity.
- `run-screenshot.png`: PNG screenshot generated from `run.log` for submission convenience.
- `run-custom-command.log`: additional runtime log from a second peer session.
- `run-custom-command-screenshot.png`: PNG screenshot generated from `run-custom-command.log`.
- `command-mapping.log`: output showing protocol maps `set_project_status` and `read_project_status`.
- `tx-sim.log`: runtime `cli_result` capture for `/tx --command ... --sim 1` via SC-Bridge CLI.

## Command used
```powershell
pear run . `
  --peer-store-name proof-admin `
  --msb-store-name proof-admin-msb `
  --subnet-channel proof-intercom-status `
  --dht-bootstrap 127.0.0.1:49737 `
  --sidechannels proof-room
```

Run date: 2026-02-24

## Runtime tx simulation commands
- `/tx --command '{"op":"set_project_status","status":"MVP ready","note":"first demo"}' --sim 1`
- `/tx --command "read_project_status" --sim 1`
