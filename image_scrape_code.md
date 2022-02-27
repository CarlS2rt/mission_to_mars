```python
# Find and click the full image button
full_image_elem = browser.find_by_tag('button')[1]
full_image_elem.click()
# Parse the resulting html with soup
html = browser.html
img_soup = soup(html, 'html.parser')
# Find the relative image url
img_url_rel = img_soup.find('img', class_='fancybox-image').get('src')
img_url_rel
# Use the base URL to create an absolute URL
img_url = f'https://spaceimages-mars.com/{img_url_rel}'
img_url

```

