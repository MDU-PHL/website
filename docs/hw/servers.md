# Servers

MDU currently has three compute servers:

* marvin: `marvin.mdu.unimelb.edu.au`
* trillian: `trillian.mdu.unimelb.edu.au`
* zaphod: `zaphod.mdu.unimelb.edu.au`

Each has 72 `Intel(R) Xeon(R) CPU E5-2699 v3 @ 2.30GHz` CPUs, and 384GB of available RAM.

We are running RedHat Enterprise Linux 7 (`RHEL7`).

The `/home` mount is mirrored across all three servers. So, what you do on one server
is visible to you on any of the other two servers. We currently have 80T of disk space
on the `/home` mount, and an additional 40T for storing read data. As of 23 August 2016,
we were 83% full on `/home` and 76% on our additional storage.

## Connecting to the servers

You can connect to the server using `ssh`:

`ssh <uom_id>@<server_name>.mdu.unimelb.edu.au`

It is recommended that you add the `-XY` flags to allow `X11` forwarding.

For example:

`ssh -XY jdoe@marvin.mdu.unimelb.edu.au`

This would connect the user `jdoe` to `marvin` and allow `X11` forwarding.

## Server use policy

Currently, the servers are under a **fair use** policy. So, we have not imposed any
queueing system like `SLURM`, or `Torque`. This means we rely on our users to work
nicely with each other. **This policy may change in the future.**

Under our current **fair use** policy, please observed the following:

When running anything, please run `top` or `htop` to certify yourself that the chosen
server does not already have a number of on-going processes. If there is high load, 
choose another server.

**ALWAYS** run your processed with `nice`. For example:

`nice blastn -query myfasta.fasta -db nr`

This will make sure that `blastn` is run with a lower priority than it would 
normally run, and thus not hog resources from others.

In the event that `research` use conflicts with `MDU` use, `MDU` will take precedence.
That means that we reserve the right to `kill` any jobs that are interfering with 
our ability to deliver on `MDU` business. In the event we need to `kill` any jobs, we
will attempt to communicate with `user`, however we make no guarantees.
