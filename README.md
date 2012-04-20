py-plex
=======

Python wrapper for the Plex Media Server http/xml API.

This is work in progress (in its early stage).


#### Some examples of what you can currently do:

	from server import Server

	server = Server(ip_address, 32400)      # insert your Plex server's ip address
	client = server.clients[0]              # get first client

	section = server.library.shows[0]       # get first TV Shows section
	shows = section.getContent('newest')    # sort shows by 'newest'
	season4 = shows[0].getSeason(4)         # get season 4 of first show in list
	episode = first_season.episodes[0]      # get first episode

	print episode.title, episode.summary    # print title and summary

	client.playVideo(episode)               # start playing this episode on client
	client.runCommand('pause')              # pause client
	client.runCommand('skipNext')           # next episode
	client.runCommand('stop')               # stop playback


    results = server.library.findMovies('Die Hard')   # returns a list of matching movies


           
