# Spotify CLI

This thing rocks!

From https://gist.github.com/wandernauta/6800547, incredible, thank you so much to the creator and commenters who suggested updates!!

## Usage:
Copy the script to somewhere in your path:

```sh
# Pick somewhere in your path, I used /usr/local/bin
echo $PATH

# Create file there, then copy /control-spotify.sh contents into it
# You might need sudo, use with care
# Use vi or whatever editor you want
# Whatever you name the file (I used sp) is how you will use it
vi /usr/local/bin/sp

# Make it executable (same, might need sudo)
chmod +x /usr/local/bin/sp
```

[Get yourself some credentials](https://github.com/spotify/web-api/issues/1372#issuecomment-546391527):

- Generate a client ID and secret for an app using [spotify developer dashboard](https://developer.spotify.com/documentation/general/guides/app-settings/#register-your-app)
- Base64 encode the them joined by a `:`, like `base64encode(client_id:secret)`
- Store this base64 encoded string in `~/.bashrc` or similar (`~/.zshrc` if you use zsh) like
```sh
export CREDENTIALS=<your beautiful encoded string>
```
- Reload to get CREDENTIALS available: `source ~/.bashrc`

Use it!!
- `sp moonshine caravan palace`
- `sp business casual`
- `sp current`

Etc - use plain `sp` to see all the options.

## Follow the dev saga
I had a [fun time blogging](https://heatherbooker.github.io/blog/2020/04/19/how-to-control-spotify-from-the-command-line.html) about the process of getting this to work this first time!

## Dev To do:

Doesn't work:
- `sp url` (prints http://open.spotify.com/track/ with Honey I'm Good (or anything else, it seems) playing)
