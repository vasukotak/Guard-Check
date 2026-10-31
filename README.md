# Guard Check

A small phone app for the night security guards (10 PM to 7 AM). The guard
takes a photo **inside the app**, and the app stamps it with:

- the **time and date, taken from the internet**, not from the phone, so
  changing the phone's clock can't fake it
- the **location** (GPS)
- the **factory** and the **guard's name**

The guard then taps **Send to WhatsApp** and sends it to the usual group.

There is no gallery button. The app only accepts a photo taken by the live
camera at that moment, so an old photo can't be sent through it.

Nothing to install for the owner. Nothing is stored anywhere except the
guard's name and factory, which stay on the guard's own phone.

## How to spot cheating in the WhatsApp group

1. **Was it sent through the app?** Every genuine photo has the dark band at
   the bottom with time, factory, guard and location. A photo without it
   wasn't taken in the app. Ask them to resend.
2. **Does the stamped time match the WhatsApp time?** They should be within
   a minute or two. A big gap means the photo was taken earlier and sent
   later.
3. **Red text on the photo?** `PHONE TIME - NOT VERIFIED` means there was no
   internet, so the time could be faked. `LOCATION NOT AVAILABLE` means
   location was off. Ask them to fix it and resend.
4. **Location:** the WhatsApp message also carries a Google Maps link. Tap
   it to see where the photo was taken.

### Random checks

Whenever you like, post **CHECK** in the group. The guard has 10 minutes to
send a fresh photo from the app. Because the time on the photo comes from the
internet, it proves the photo was taken *after* your message. Do this at
unpredictable times, and they can't rely on an alarm.

## Guard instructions (forward this on WhatsApp)

> **Night check photo — how to use**
>
> 1. Open this link in **Chrome**: https://vasukotak.github.io/Guard-Check/
> 2. Type your name, choose your factory, press **Save**. (Only the first time.)
> 3. Press **Allow** for camera and location. Keep phone **Location ON** and **mobile data ON**.
> 4. Chrome menu (⋮) → **Add to Home screen**. Now open it from that icon every time.
> 5. Every check: open the app → **Take photo** → **Send to WhatsApp** → choose our group → send.
>
> **रात की चेक फोटो — कैसे भेजें**
>
> 1. यह लिंक **Chrome** में खोलें: https://vasukotak.github.io/Guard-Check/
> 2. अपना नाम लिखें, अपनी फैक्ट्री चुनें, **Save** दबाएं। (सिर्फ पहली बार)
> 3. कैमरा और लोकेशन के लिए **Allow** दबाएं। फ़ोन की **Location** और **mobile data** चालू रखें।
> 4. Chrome मेनू (⋮) → **Add to Home screen**। हर बार उसी आइकन से खोलें।
> 5. हर चेक पर: ऐप खोलें → **फोटो लें** → **व्हाट्सएप पर भेजें** → ग्रुप चुनें → भेजें।

## Optional: "at factory" check

If you send the Google Maps location of each factory, the app will also print
**At Agarbatti Factory** on the photo, or in red **2.3 km AWAY FROM AGARBATTI FACTORY** if
it was taken somewhere else. To set it, fill in `lat` and `lng` for each
factory near the top of the script in `index.html`. Factory names can be
changed in the same place.

## Hosting

The camera and GPS only work on a secure (`https://`) website. This folder is
a plain website with no server or database, so any free static host works.
For example, put it in its own **public** GitHub repository and turn on
GitHub Pages. The folder contains no business data, so it's safe to make
public.
