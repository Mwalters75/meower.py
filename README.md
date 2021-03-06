# meower.py
Python library for interacting with the Meower API
## Commands
- `meower.repair_mode()` - Checks if the server is in repair mode
- `meower.scratch_deprecated()` - Checks if Scratch clients are now deprecated
- `meower.find_post(num)` - Downloads home, then finds the post number
- `meower.get_home()` - Downloads home, in a JSON array
- `meower.home_len()` - Shows the number of posts on home
- `meower.get_post(str)` - Gets the specified post, and shows in `username: post` format
- `meower.page_len()` - Shows the number of home pages
- `meower.current_page()` - Returns the current page number
- `meower.change_page(num)` - Changes the page
- `meower.ping()` - "Pings" the Meower API, by timing `requests` to fetch the root page 
- `meower.argo_tunnel()` - Checks if there is a Argo Tunnel error on the API
- `meower.get_pfp(str)` - Downloads the specified user's profile picture
## Installing
`meower.py` is now on [PyPI](https://pypi.org/project/meower/)! That means that you can use `pip3` to install it, now!
```
pip3 install meower
```
## Usage
To import, just simply use the following:
```python
import meower
```
## Building
Before you build, you'd might want to double-check that you have all of the dependencies:
```
pip3 install -r requirements.txt
```
Run the `build` command:
```
python3 -m build
```
## Upgrading
`meower.py` is a ongoing project, so you'd might want to check for updates regularly. You can update the package like this:
```
pip3 install --upgrade meower
```
## Demo Client
```python
import meower

for i in range(0, meower.home_len()):
	print(meower.get_post(meower.find_post(i)))
```
