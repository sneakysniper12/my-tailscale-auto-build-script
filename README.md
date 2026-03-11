# my-tailscale-auto-build-script
the script i built and use to have a simple one line install script for linux

You'll need to generate your own auth key and api key for your tailnet.
to do this:
1. Go to your tailnet admin console
2. Go to settings
3. Click "keys" in the personal settings tab
4. open your notes app to copy the keys to
5. generate an Auth key and copy it in the notepad
6. generate an api key and paste it in the notepad


this took afew tries to get right, but here's the all in one code:
  
  export AUTH_KEY="your AUTH key"
  export API_KEY="your API key"
  
  curl -fsSL https://raw.githubusercontent.com/sneakysniper12/my-tailscale-auto-build-script/main/install-tailscale.sh | sudo AUTH_KEY="$AUTH_KEY" API_KEY="$API_KEY" bash
