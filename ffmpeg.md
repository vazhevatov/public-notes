

ffmpeg -i original.mp4 -vf scale=848:480 -preset slow -crf 18 modified.mp4

ffmpeg -i original.mp4 -b:a 192K -vn out.mp3

ffmpeg -ss 00:00:00 -to 00:02:16 -i original.mp4 -c copy out.mp4

ffmpeg -protocol_whitelist file,http,https,tcp,tls,crypto -i master.m3u8 -c:v libx264 -c:a mp3 -c copy out.mp4

ffmpeg -i video.mp4 -i audio.mp3 -c:v copy -map 0:v -map 1:a -y out.mp4

ffmpeg -i input.wav -vn -ar 44100 -ac 2 -b:a 192k out.mp3

ffmpeg -fflags +genpts -i input.webm -r 24 out.mp4

ffmpeg -i input.mp4 -filter_complex "[0:v]pad=1280:720:-1:-1,fps=30000/1001[v];[0:a]aformat=sample_rates=44100:channel_layouts=stereo[a]" -map "[v]" -map "[a]" out.mp4

ffmpeg -f lavfi -i color=size=1280x720:rate=25:color=black -f lavfi -i anullsrc=channel_layout=stereo:sample_rate=44100 -t 10 black.mp4 # -t 10 = 10 seconds

ffmpeg -f concat -i list.txt -c copy out.mp4
$ cat list.txt
file '1.mp4'
file '2.mp4'
file '3.mp4'
