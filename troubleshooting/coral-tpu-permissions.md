# Coral AI chip losing its permissions after a reboot

## What happened

My camera system uses a Coral chip to spot people and cars. It worked fine after setup, but every time the Pi rebooted, detection stopped. The camera software couldn't open the chip anymore.

## How I tracked it down

The cameras were still recording, so I knew the problem was only the AI part. The logs showed a permission error when the software tried to open the chip. I checked the device and saw it was coming back after each reboot owned by the wrong group, so the camera software wasn't allowed to use it. I had fixed it by hand once before, which is why it worked until the next restart.

## The fix

I set up a rule so the system gives the chip the right group every time it starts, and made sure the camera software's user was in that group. After that I rebooted a few times to be sure detection came back on its own.

## What I took from it

If something works until a reboot, the fix you made was temporary. Find the setting that gets applied at startup and fix it there.
