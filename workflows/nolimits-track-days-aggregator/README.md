# No Limits Track Days Events Aggregator

A scheduled n8n automation workflow that aggregates upcoming track day events from No Limits Track Days across multiple UK circuits and delivers a formatted HTML email digest.

## Purpose

This workflow automatically checks availability for track days at 10 UK racing circuits, validates and aggregates the data, then sends a comprehensive email report highlighting available events, limited spaces, and booking information.

## How It Works

1. **Schedule Trigger** - Runs daily at a configured time
2. **Configuration** - Centralized settings for tracks, API endpoints, thresholds, and styling
3. **API Endpoints** - Generates URLs for 10 UK tracks (Brands Hatch, Silverstone, Donington, etc.)
4. **Fetch Data** - Retrieves event availability from each track's API
5. **Validate** - Ensures data quality and filters invalid events
6. **Aggregate** - Combines all events, sorts chronologically, and calculates statistics
7. **Generate HTML** - Creates a mobile-responsive email with event details and booking links
8. **Send Email** - Delivers the report via SMTP

## Features

- 📊 Summary statistics (total events, limited spaces alerts)
- 📅 Chronologically sorted events by track and date
- ⚡ Visual indicators for limited availability
- 📱 Mobile-responsive email design
- 🔗 Direct booking links
- ✅ Robust error handling and data validation

## Setup Instructions

### Prerequisites

- n8n instance (self-hosted or cloud)
- SMTP credentials for sending emails

### Configuration

1. **Import the workflow** into your n8n instance
2. **Configure email settings** in the "Send email" node:
   - Set `fromEmail` to your sender address
   - Set `toEmail` to your recipient address
3. **Add SMTP credentials**:
   - Go to Credentials → Add Credential → SMTP
   - Configure your SMTP server details
   - Assign the credential to the "Send email" node
4. **Adjust schedule** (optional):
   - Modify the "Schedule Trigger" node to set your preferred time
5. **Customize settings** (optional):
   - Edit the "Configuration" node to adjust thresholds, styling, or track list

### Testing

After setup, use the "Test workflow" button in n8n to verify everything works correctly before activating the schedule.

## Tracks Monitored

- Brands Hatch
- Cadwell Park
- Croft
- Donington Park
- Oulton Park
- Silverstone
- Snetterton
- Thruxton
- Mallory Park
- Rockingham

## Notes

- The workflow includes retry logic for API failures
- Empty responses (no events) are handled gracefully
- Invalid or incomplete event data is filtered out during validation
- All configuration is centralized in the "Configuration" node for easy maintenance

## License

Feel free to use and modify this workflow for your own purposes.
