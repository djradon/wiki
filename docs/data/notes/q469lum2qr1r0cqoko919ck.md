

- [[can be extended by|p.hasExtensionMechanism]]
  - plugin
    - [[p.hadAtLeastOneOf]] 
      - server component 
        - runs as a server subprocess
        - written-in: #go
      - "web app" component
        - included in page, runs alongside the Mattermost web app code
          - desktop app is shim of web app
        - written-in: javascript
        - [[p.builtOn]] 
          - [[prdct.react]]
          - [[prdct.redux-js]]
  - app
    - lightweight interactive "add-ons" 
    - in any language
    - receive webhooks from mattermost and 3rd-parties
    - use Mattermost REST APIs to post messages
    - attach them selves to locations the user

- Chose mysql technology for openness.
- our web hooks and slash commands are binary level protocol compatible with Slack.
  - [[p.hasSource]] https://go.theregister.com/feed/www.theregister.com/2022/05/26/mattermost/