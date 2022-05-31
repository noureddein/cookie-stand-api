# Lab 34: API Deployment

## Feature Tasks and Requirements

### Use API Quick Start Template
- [x] Create a new repo cookie-stand-api that uses [API Quick](https://github.com/codefellows/python-401-api-quickstart) Start as a template.
- [ ] Modify your application using instructions in README.md found in root of repo.
    - [x] Change **things** app folder to be **cookie_stands**
    - [ ] Go through code base looking for Thing,thing and things change to cookie-stand related names.
    - [x] E.g. Thing model becomes CookieStand
    - [x] E.g. ThingList becomes CookieStandList
- [x] Pro Tip: Do a global text search looking for thing
    - Search should be case insensitive.

### Deeper CookieStand Changes
- [x] The CookieStand model must contain:

```python
    location = models.CharField(max_length=256)
    owner = models.ForeignKey(
        get_user_model(), on_delete=models.CASCADE, null=True, blank=True
    )
    description = models.TextField(default="", null=True, blank=True)
    hourly_sales = models.JSONField(default=list, blank=True)
    minimum_customers_per_hour = models.IntegerField(default=0)
    maximum_customers_per_hour = models.IntegerField(default=0)
    average_cookies_per_sale = models.FloatField(default=0)
```

### Database Deployment Requirements
- [x] Host your Database at [ElephantSQL](https://www.elephantsql.com/)

### Site Deployment Requirements
- [x] Deploy Docker container to Heroku

### Implementation Notes
- [x]  Site must use environment variables.

### Useful Terminal Commands
- `docker-compose up --build`
- `docker-compose down`
- `docker-compose restart`
- `docker-compose run web python manage.py migrate`
- `docker-compose run web python manage.py collectstatic`

### User Acceptance Tests
- Manually confirm API using API Tester, Postman or HTTPie.
- Remember to use deployed url, not localhost


### [PR](https://github.com/noureddein/cookie-stand-api/pull/1)
