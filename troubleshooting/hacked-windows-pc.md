# Cleaning up a hacked Windows PC for a client

## What happened

A client's Windows computer had been taken over. Someone was getting in remotely and using it to steal passwords.

## How I tracked it down

I went through the user accounts on the machine and found five admin accounts the client didn't create. Those accounts were being used to log in remotely with Remote Desktop.

## The fix

I removed all five accounts, shut off the remote access the attacker was using, and locked down how the machine can be reached from outside. I had the client change their passwords. Then I wrote up what I found and what I changed so they had a record of it.

## What I took from it

The cleanup is only half the job. Writing it down means the client knows what happened and the next tech doesn't have to start over.
