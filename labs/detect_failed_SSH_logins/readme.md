# Detect failed SSH logins

## what does it do
- simple bash script that checks Linux auth logs for failed SSH login attempts

## how it works
- looks into /var/log/auth.log
- finds lines with 'Failed Password'
- extracts the source IPs and counts how many times each IP failed
- sorts the list by most suspicious IPs

- still pending for the files to upload
