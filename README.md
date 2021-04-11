# Schmudo Fake Checkins

Just show a nice QR-Checkin-Page for those ones who want to scan your data.

## Credits:
* z85-encoding-snippet:
 * https://github.com/michaelrhodes/z85.git (MIT)
* qrcodejs
 * https://github.com/davidshimjs/qrcodejs.git (MIT)
 * see submodule

## Missing something?

I did not include the Logo on purpose.
Just design your own one or find one [on the internet](https://app.luca-app.de/webapp/static/media/LucaLogoWhite.68e3f825.svg).

## How it started?

[Somebody](https://twitter.com/AllenRe97883617/status/1379405366010732552 "Somebody") postet a single line on Twitter:

```bash
FOO=$(echo 030101$(printf '%x' $(date +%s)|sed 's/\(..\)/\1\n/g'|tac)$(dd if=/dev/urandom count=89 bs=1 2>/dev/null|xxd -ps)|tr -d ' '); echo $FOO$(echo $FOO|xxd -r -ps|sha256sum|head -c 8)|xxd -r -ps|basenc --z85|qr

```