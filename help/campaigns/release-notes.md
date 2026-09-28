---
description: Learn about feature enhancements and fixes in the Adobe CX Enterprise Coworker Campaigns release notes.
title: CX Enterprise Coworker Campaigns Release Notes
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Adobe CX Enterprise Coworker Campaigns release notes {#release-notes}

Coworker Campaigns releases operate on a continuous delivery model which allows for a more scalable, phased approach to feature deployment.

## September 2026 {#sep-2026}

**Release date: September 17, 2026**

* Connect a Databricks workspace hosted on Azure, GCP, or a custom domain
* Campaigns can no longer be launched until their workflow is fully set up
* Campaign templates have been refreshed with updated content
* Choose a connector directly while uploading your contact list CSV
* Fixed a crash that could happen after scrolling through a long list of trial signups
* Fixed an issue where uploading an audience CSV with blank or duplicate headers could crash the page
* Fixed placeholder text in a campaign prompt that showed up unfilled after being resolved
* Fixed a crash on the Skills page caused by a missing color gradient
* Fixed chat getting stuck repeating the same question after you already answered it
* Chat responses no longer show a stray ID prefix in front of your selected answer
* Chat now suggests quick next-step replies you can tap to fill the compose box
* Campaign templates now open in a streamlined in-page view instead of a separate dialog
* The expanded chat progress bar now scrolls internally instead of pushing your conversation out of view
* Campaign settings now reflect the latest board details more accurately
* The upgrade-plan dialog now uses a more consistent look and feel
* Removed a redundant status indicator from the campaign plan header for a cleaner look
* Rapid email edits are now saved together as a single version-history entry instead of many
* Fixed brand kit titles occasionally blanking out while a draft was being generated
* Edit an image with Adobe Express directly from the image toolbar
* Basic agent audience data now stays in sync on the campaign board without a manual refresh
* Brand logos on the campaign board are cropped more neatly to fit their space
* Smoother visual handoff when your campaign plan moves onto the campaign board

**Release date: September 3, 2026**

* Copy any chat message and rate AI responses with a thumbs up or thumbs down, right from the message itself
* The campaign plan task list now stays pinned above the chat input while your campaign is running, so you can track progress without scrolling away
* Connect a Databricks SQL warehouse as a new data source for your campaigns
* The older chat-based email editor has been retired in favor of the newer email asset editor
* Trial User Admin now lets you exclude Adobe users, making it easier to see real trial signups
* Fixed an issue where similar-campaign suggestions could fail to load
* Chat messages now have tighter, more consistent spacing

**Release date: September 1, 2026**

* Large campaign emails now display fully in the editor instead of being cut off
* The campaign board's launch button is now labeled "Review and launch" for clarity
* Connecting a Salesforce account no longer shows an incorrect Marketo error message
* Salesforce now has its own logo in the connectors list
* Available connectors are now listed ahead of coming-soon ones
* Onboarding now shows a progress indicator while your brand kit loads
* Audience and knowledge-source previews now have a close button and can open full-screen
* Campaign plan cards no longer get stuck showing "building" after your campaign starts running
* Chat no longer keeps temporary progress messages (like "Exploring…") in your conversation history
* Toolbar controls now lock appropriately while AI image or text suggestions are being applied
* Fixed an issue where replacing an image in the asset editor didn't work correctly

## August 2026 {#aug-2026}

**Release date: August 26, 2026**

* Clicking anywhere on a campaign template card now opens its preview, not just the title
* The campaign prompt bar placeholder reappears correctly after you clear your input, with clearer screen-reader support
* The "Help me prompt" suggestion now correctly replaces existing text in the campaign prompt bar
* Downloading unsubscribes as a CSV now reflects only the campaign execution you're viewing
* The trial plan comparison now shows Launch campaigns and Campaign insights as included features
* Audiences created without a full workflow now show up correctly on the campaign board's Audience card
* Empty-state feedback prompts read more naturally throughout the app

**Release date: August 25, 2026**

* Signing in on one browser tab now syncs the others automatically, fixing account mix-ups between tabs
* Clicking Build now reliably moves your plan forward instead of occasionally re-generating it
* Workflow diagrams in chat show more of the canvas so zoom controls no longer cover the steps
* Campaign detail tabs have a refreshed, more consistent look
* Saving or removing a sending domain in Domains & Senders is now faster and more reliable

**Release date: August 24, 2026**

* See your generated campaign strategy directly on the campaign board
* Replace your audience right from the campaign validation dialog
* Campaign PDF and Word exports now include your real workflow diagram
* Insights tab stays visible with a helpful empty state right after launch
* Add or remove touchpoints while reviewing your campaign fields
* Campaign board toolbar is simpler with unnecessary buttons removed
* Domains & Senders wizard scrubs subdomains and guides first-time setup with a coachmark
* Domains & Senders wizard shows subdomain validation errors inline as you type
* The post-proof campaign call-to-action was removed for a cleaner flow
* Chinese language names now display correctly in the language picker
* AI-generated variant thumbnails load reliably without duplicate labels
* Newly created campaigns now show up immediately in your recent campaigns list on Home
* All-campaigns insights now include an AI-generated summary of your org's campaign performance
* Providing requested input in a workflow conversation no longer leaves it stuck
* Trial onboarding no longer flashes an extra loading screen while checking for an existing brand kit
* Stale sample audience sources now clear automatically from your workflow
* Layout, theme, and fonts now render correctly inside the unified Experience Cloud shell
* Similar campaign suggestions no longer show an unnecessary channel field

**Release date: August 14, 2026**

* Delete draft domains you no longer need in Domains & Senders
* See DNS verification status for each record during domain setup
* Domain details now show your configured email sender
* DNS record values truncate neatly with a tooltip for the full text
* Format multiple email text blocks at once with multi-select
* Get similar campaign suggestions when creating a new campaign
* Scope campaign insights to a single execution of a recurring campaign
* Choose your preferred language from the profile menu
* Get a nudge when campaign template descriptions need more detail
* Release notes are easier to browse with better navigation and pagination
* Collapse the sidebar's recent campaigns list to save space
* Your campaign inventory view now stays the way you left it
* Reorder execution filters and jump to a date range from a calendar picker
* Preview audience details even on read-only audience cards
* Fixed onboarding trial-flow screen flashes and a sign-in timing issue
* Chat rail resize handle no longer blocks the message list scrollbar
* Brand kit creation now shows the real reason a save failed

**Release date: August 6, 2026**

* Campaign Insights now shows unsubscribes with a downloadable CSV of who opted out
* A per-email performance breakdown table is now on the Insights tab
* See your campaign journey map directly on the Insights tab
* Duration-based wait steps are now visible in the journey workflow view
* Weighted journey branches are shown in the workflow edit view
* Contact Lists are now connected to live data
* Recurring campaigns show 0 sends immediately instead of "insights pending"
* Edit remix prompt text directly around placeholder chips
* Improved coachmark and cleaner placeholder chips in the remix editor
* Campaign workflow cards now show a helpful empty state when nothing is running
* The upgrade plan button no longer clutters the campaign detail header
* Workflow cards have a simpler layout with journey name and description removed

## July 2026 {#july-2026}

**Release date: July 30, 2026**

* All-campaigns insights now match individual campaign insights' layout, plus a new daily performance chart
* Stop a live campaign directly from the campaign page
* Duplicating a campaign now only asks for a new name
* Edit email templates directly from the templates list
* Filter the recurring campaign journey view by execution
* Add a brand image directly from the campaign board
* Trial admin table now supports email search, pagination, and full CSV export
* The "Surprise me" button now responds instantly, with no animation delay
* Removed the campaign email unsubscribe settings while we rework this feature
* Edit a campaign's schedule after it's already set, without starting over
* Open the writing style editor from the overflow menu for quicker access
* Pressing Enter now submits consistently across every prompt bar in the app

**Release date: July 23, 2026**

* Schedule campaigns to send right away, once at a chosen time, or on a recurring basis
* Manage unsubscribe lists from Contact Lists and set unsubscribe parameters in campaign email settings
* Build and manage forms with a new forms inventory and editor
* Connector setup shows clearer guidance when credentials fail, including when updating an existing connection
* Marketo connections now support Experience Cloud URLs
* Domains & Senders wizard catches more DNS record issues before your domain goes live
* Add connectors directly from the campaign input's add menu
* Inventory pages show friendlier illustrated empty states when there's nothing to show yet
* Campaign insights show which data source powers each metric
* Brand editors are now built into onboarding for a smoother first-time setup
* Preview a sample audience before you commit to your campaign
* Coworker Campaigns now lives inside the unified Experience Cloud navigation shell
* Removed the floating feedback tip bar for a cleaner campaign board
* Various performance and reliability improvements throughout

**Release date: July 14, 2026**

* Domains & Senders rollout, live workflow progress, and real campaign insights
* Domains & Senders setup is now fully available, with your sender choice saved automatically
* Choose or update your campaign's email sender right from campaign settings
* The Senders tab stays browsable even before a domain is verified
* Email drafts added mid-conversation now reliably appear on the campaign board
* Help and feedback are combined into one streamlined popover
* Starting a new conversation no longer shows leftover messages from the last one
* Multi-turn conversations no longer show outdated prompts in the response drawer
* Numbered lists in chat messages keep their correct order
* HubSpot connector setup now asks for a service key, matching HubSpot's own terminology
* The trial admin table shows a user count and no longer clips the last row
* Various performance and reliability improvements throughout

**Release date: July 9, 2026**

* A maintenance banner and dialog now warn you ahead of scheduled downtime
* Domains & Senders has a guided setup wizard for verifying domains and adding senders
* Draft campaigns now prompt you to finish email and channel setup before you send
* Domain and sender validation catches more issues, including DNS record edge cases
* The profile menu has moved to the sidebar for quicker access
* Source PDF documents now show as a pill on brand kit details
* Various performance and reliability improvements throughout

**Release date: June 26, 2026**

* A new Insights dashboard shows campaign performance KPIs: sends, opens, clicks, bounces, and more
* Campaigns show a live status badge on the board so you can see active sends at a glance
* Contextual tips appear in the campaign board to guide you through next steps
* New-user onboarding uses your real brand data to personalize the setup experience
* Brand color picker handles shorthand hex codes and opens in a tidy popover
* UTM parameters and message capping are now configurable from App Settings
* Help links now open the latest content directly on Experience League
* Various performance and reliability improvements throughout

**Release date: June 24, 2026**

* Launching a campaign now triggers a confetti celebration
* Campaigns show a status badge and the board locks to read-only once launched
* Brand overview fits your screen with empty-state prompts and better logo display
* Validation shows a clear dialog even when an unexpected error type is returned
* Generated email content uses your campaign goal for more relevant results

## June 2026 {#june-2026}

**Release date: June 23, 2026**

* A validation step checks that your campaign is ready before you launch
* See why each email variant was created with a new variation rationale
* Campaign plan view shows a live milestone progress rail as tasks stream in
* New-user onboarding uses your real brand data to personalize the setup experience
* Brand color picker handles shorthand hex codes and opens in a tidy popover
* UTM parameters and message capping are now configurable from App Settings
* Help links now open the latest content directly on Experience League
* Various performance and reliability improvements throughout

**Release date: June 19, 2026**

* Check email client compatibility for every element before you send
* Browse and restore previous versions of your email with a new version history panel
* Edit brand colors with a hex-first picker and inline editing on the brand page
* Brands library loads more brands automatically as you scroll
* The profile menu has moved to the sidebar for quicker access
* Source PDF documents now show as a pill on brand kit details
* Various performance and reliability improvements throughout

**Release date: June 12, 2026**

* Browse product help and guides without leaving the app
* Campaign plans appear section by section as they are generated
* Pick up campaign conversations where you left off more reliably
* Launch campaigns from a dedicated dialog when your plan is ready to go
* Onboarding uses clearer product naming and home prompt guidance
* Connector setup shows the right fields for API key and sign-in connections
* Out-of-scope chat replies suggest what to ask next with one-click prompts
* Campaign PDF exports show icons, product branding, and a brand label reliably
* Talk to an expert and upgrade flows load your trial details more reliably
* Writing style tags expand to show full text and link to your brand page
* Start a brand from the empty library state with helpful categories
* Sign in again smoothly when your session expires
* The app now lives at coworker-campaigns.adobe.com with the same experience
* Trial sign-up routes you to the right next step after creating your account
* Various performance and reliability improvements throughout

**Release date: June 11, 2026**

* Coming-soon pages show a clean placeholder without background clutter
* Email editor toolbars look right in light theme
* Deleting an email image clears the selection so the toolbar disappears
* CSV audience imports no longer show a duplicate list in the audience card
* The Chats item in the sidebar highlights when you start a new chat
* The app header now shows just the email subject (or "Draft") when editing an email, removing the "Email N:" number prefix for a tidier title
* The profile menu has moved to the sidebar for quicker access
* Source PDF documents now show as a pill on brand kit details
* Various performance and reliability improvements throughout

**Release date: June 10, 2026**

* The app is now Coworker Campaigns with updated naming throughout
* A first-time onboarding tour walks you through building a demo brand
* Launch campaigns from a dedicated dialog when your plan is ready to go
* Connect HubSpot with an API key from the integrations catalog
* Browse chats with a redesigned conversation list and clearer empty states
* Undo and redo email edits with familiar keyboard shortcuts
* Retry saving when the email editor hits a temporary error
* Replace email images with correct sizing and Adobe Express dimensions
* Upload audience lists from CSV using a clearer import dialog in chat
* Writing style tags expand to show full text and link to your brand page
* Start a brand from the empty library state with helpful categories
* Sign in again smoothly when your session expires
* Various performance and reliability improvements throughout

**Release date: June 9, 2026**

* Compare trial usage and upgrade options in a redesigned plan dialog
* Browse and manage data connectors from a live catalog in the app
* Fill in general settings and notification preferences in Settings
* Your sign-in stays fresh with a clear prompt when your session expires
* Your email address appears automatically when sending a test email
* Confirm before making a brand kit your default
* Brand kit uploads now respect a 100 MB file size limit
* Edit your campaign name directly on the campaign board
* Preview templates and confirm before you send a campaign
* Various performance and reliability improvements throughout

**Release date: June 4, 2026**

* Recent chats appear in the sidebar and you can rename them inline
* Open the Chats page to search and continue past conversations
* Home workflows are now campaign templates with a simpler remix flow
* Library templates use a clearer table with descriptions and channel filters
* Brand kits show your default first and filter by published or draft
* After publishing a draft brand, you land on the live brand kit automatically
* Campaign and brand data load more reliably right after you sign in
* Various performance and reliability improvements throughout

## May 2026 {#may-2026}

**Release date: May 29, 2026**

* Generate image variants and pick from your own images right inside the email editor
* Add images from your computer using a local file picker in the image toolbar
* Describe what you want and let AI generate the perfect image for your email
* Export your finished email as an HTML file from the More menu
* Smart copy suggestions now appear in the email toolbar as you edit text
* Click a brand on the campaign board to instantly view brand details
* Set your default brand kit directly from the Library
* Emails in the editor now follow the workflow sequence for a clearer order
* Home screen file attachments are now limited to PDFs for reliable processing
* Keyboard navigation, screen reader support, and motion preferences are more consistent throughout the app
* Coming-soon labels mark pages that are being actively built
* Various performance and reliability improvements throughout

**Release date: May 21, 2026**

* Edit email images with Adobe Express without leaving the editor
* Create brands with clear progress while assets are extracted and published
* Manage domains and senders from the People section
* Browse and manage contact lists from the People section
* Switch asset templates when working with marketing assets
* Download campaign plans as Word files with workflow diagrams
* Lists across campaigns, skills, and workflows share a clearer layout
* Various performance and reliability improvements throughout

**Release date: May 14, 2026**

* Library brings Assets, Templates, and Brands together in one place
* Sidebar and navigation make audiences and your default brand kit easier to reach
* Download your campaign plan as a PDF right from campaign details
* Brand editing opens clearer panels for overview, writing style, and colors
* Trial countdown appears in the header so remaining days stay visible
* Sports marketing workflows are ready when your brief fits that category
* Manual trial setup handles company website addresses more predictably
* Various performance and reliability improvements throughout

**Release date: May 8, 2026**

* Campaign chat offers a clear retry when a background task check fails
* Task status updates and fullscreen layout feel smoother on campaign boards
* The app starts faster by loading routes and translations as you need them
* Campaign and brand data remain consistent across the app
* Undo and redo email edits work more predictably
* Retry saving when the email editor hits a temporary error
* Replace email images with correct sizing and Adobe Express dimensions
* Upload audience lists from CSV using a clearer import dialog
* Writing style tags expand to show full text and link to your brand page
* Various performance and reliability improvements throughout

**Release date: May 6, 2026**

* Campaign boards and lists stay aligned with the latest details as you are working
* A clear generative AI disclaimer appears in campaign chat and Agent Builder
* Support contact details now use the dedicated CX Coworker Campaigns email address
* The marketing home page removes the waitlist section and shows the hero video more clearly
* More screens respect your language and local date formats automatically
* Various performance and reliability improvements throughout

## April 2026 {#apr-2026}

**Release date: April 28, 2026**

* Campaign lists and boards stay in sync and feel snappier when you open or update a campaign
* Home workflows are now campaign templates with a simpler remix flow
* Dark and light themes use refreshed Spectrum styling for a more consistent look across the app
* Chat handles empty assistant content gracefully, with smoother status animations and clearer status animations
* Restored conversations open without a blank chat rail flash, and switching email variants no longer flickers the rail
* File upload controls step out of the way after you send or continue the conversation
* "Help me write" fetches prompt ideas only after you open the popover
* Status updates only show an expand control when there is a list to reveal
* Cards across campaigns, skills, and workflows share a more consistent layout
* Campaign lists and brand data load more reliably right after you sign in
* Various performance and reliability improvements throughout

**Release date: April 19, 2026**

* The app header now shows just the email subject (or "Draft") when editing an email, removing the "Email N:" number prefix for a tidier title
* The profile menu has moved to the sidebar for quicker access
* Source PDF documents now show as a pill on brand kit details
* The profile menu has moved to the sidebar for quicker access
* Various performance and reliability improvements throughout

**Release date: April 18, 2026**

* The home page campaign input now has an animated glow ring and a taller, brighter hero gradient
* "Surprise me" triggers a colorful gradient shimmer on the input border
* The app now supports a more consistent layout across product pages
* Documentation links now open the latest content directly in a new tab
* Various performance and reliability improvements throughout
