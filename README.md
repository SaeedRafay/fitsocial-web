# FitSocial Web

This is the web landing page for the FitSocial mobile app. It serves two purposes:

1. A landing page for the app with download links
2. A way to share activities from the app via web links

## How It Works

The web page has two modes:

### Landing Page Mode

When accessed without an activity ID (e.g., https://saeedrafay.github.io/fitsocial-web/), it shows:
- App description
- Feature highlights
- Download links for app stores

### Activity Sharing Mode

When accessed with an activity ID, it displays details of that specific activity:
- Activity title, description, and image
- Location and date information
- Button to open in the app (with fallback to app stores)

## How to Share Activities

Activities can be shared in two ways:

1. **Path Parameter**: https://saeedrafay.github.io/fitsocial-web/ACTIVITY_ID
2. **Query Parameter**: https://saeedrafay.github.io/fitsocial-web/?id=ACTIVITY_ID

## Technical Details

- The page uses the Supabase Edge Function `share-activity` to fetch activity data
- Deep linking is supported with the `fitsocial://` protocol
- If the app is not installed, users are redirected to the appropriate app store

## Customization

To customize this page:

1. Update the app store links in the JavaScript variables
2. Replace `app-preview.png` with an actual screenshot of your app
3. Adjust the styling in the CSS section as needed

## Testing

To test activity sharing locally:
1. Create an activity in the app
2. Get the activity ID
3. Append it to the URL as shown above 