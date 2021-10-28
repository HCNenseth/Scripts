# Scripts


How many services are listening on the target system on all interfaces? (Not on localhost and IPv4 only)

	netstat -tunlep4 | grep -v "127\.0\.0" | grep LISTEN | wc -l

Use cURL from your Pwnbox (not the target machine) to obtain the source code of the "https://www.inlanefreight.com" website and filter all unique paths of that domain.

	curl https://www.inlanefreight.com | grep "inlanefreight.com" | awk -F "https://" '{print $2}' | cut -d " " -f1 | sort -u | wc -l

change keyboard to NOR

	setxkbmap -layout no


sed -ri '/^.{,7}$/d' william.txt            # remove shorter than 8

sed -ri '/[!-/:-@\[-`\{-~]+/!d' william.txt # remove no special chars

sed -ri '/[0-9]+/!d' william.txt            # remove no numbers

SAMBA
	smbclient
		-N : no passw
		-L : avail. services
	impacket
		Impacket is a collection of Python classes for working with network protocols. Impacket
		is focused on providing low-level programmatic access to the packets and for some
		protocols (e.g. SMB1-3 and MSRPC) the protocol implementation itself. Packets can be
		constructed from scratch, as well as parsed from raw data, and the object oriented API
		makes it simple to work with deep hierarchies of protocols. The library provides a set
		of tools as examples of what can be done within the context of this library.
		
