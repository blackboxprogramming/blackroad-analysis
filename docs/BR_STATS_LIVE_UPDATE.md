# 🚀 br-stats LIVE GIT INTEGRATION

## What's New

Your `br-stats` tool is now **dynamically powered by actual git repositories**!

### ⚡ Live Features

**Automatic Git Scanning:**
- Scans all git repos on your machine
- Counts actual commits, branches, files
- Detects active repositories (commits in last 7 days)
- Calculates real metrics (avg commits per repo, etc.)

**GitHub API Integration:**
- Uses `gh` CLI to pull live GitHub data
- Real repository count from your GitHub account
- Actual organization membership
- Live star counts

**Smart Caching:**
- Updates every 5 minutes automatically
- Shows cache age in dashboard
- Instant display (no waiting)
- Manual refresh with `br-stats update`

### 📊 New Commands

```bash
# Live dashboard (auto-updates from git)
br-stats

# Force immediate update
br-stats update

# Start auto-update daemon (updates every 5 min)
br-stats-daemon start

# Check daemon status
br-stats-daemon status

# View daemon logs
br-stats-daemon logs

# Stop daemon
br-stats-daemon stop

# Save snapshot for history
br-stats-history snapshot

# List all historical snapshots
br-stats-history list

# Compare two time periods
br-stats-history compare 20260130-150000 20260130-160000

# Show growth trend over time
br-stats-history trend
```

### 🎯 What It Tracks (LIVE)

**From Local Git:**
- Total repositories on your machine
- Total commits across all repos
- Total branches
- Total files tracked
- Active repos (last 7 days)
- Average commits per repo

**From GitHub API:**
- Your actual GitHub repo count
- Organization memberships
- Total stars across repos
- Public vs private repos

**From Docker:**
- Running container count
- Updates dynamically as you start/stop containers

### 🔄 Auto-Update Daemon

Run once to keep stats always fresh:

```bash
# Start background updater
br-stats-daemon start

# Add to startup (optional)
echo "br-stats-daemon start" >> ~/.zshrc
```

The daemon:
- Updates stats every 5 minutes
- Runs silently in background
- Logs all activity to `~/.blackroad/stats-cache/daemon.log`
- Survives terminal closes

### 📈 Historical Tracking

Build a portfolio timeline:

```bash
# Take daily snapshots
br-stats-history snapshot

# Compare growth week-over-week
br-stats-history compare 20260123-120000 20260130-120000

# Output:
# Repositories:  1024 → 1094 (+70)
# Commits:       15234 → 18456 (+3222)
# Stars:         234 → 289 (+55)
```

### 🎨 Visual Improvements

**Live Indicators:**
- 📡 Cache freshness display
- ⚡ Real-time data badge
- 🔄 Update progress during refresh
- ✅ Success confirmations

**New Metrics:**
- 💻 Local git repos discovered
- ✅ Active repos (7-day window)
- 🔀 Total commits (all repos)
- 🌿 Total branches
- 📄 Files under version control
- 📈 Average commits per repository

### 🎯 Interview Power Moves

**Before Interview:**
```bash
br-stats update  # Get latest numbers
br-stats-history snapshot  # Save for later
```

**During Screen Share:**
```bash
br-stats  # Shows LIVE data with timestamps
```

**For Applications:**
```bash
br-stats json > portfolio-$(date +%Y%m%d).json
```

**Weekly Progress:**
```bash
br-stats-history trend  # Show consistent growth
```

### 📂 File Locations

```
~/.blackroad/
├── stats-cache/
│   ├── stats.json          # Current stats (auto-updates)
│   ├── daemon.pid          # Daemon process ID
│   └── daemon.log          # Update logs
└── stats-history/
    ├── 20260130-150000.json
    ├── 20260130-153000.json
    └── ...
```

### 🚀 Quick Start

```bash
# 1. Update to latest stats
br-stats update

# 2. View live dashboard
br-stats

# 3. Start auto-updater (optional)
br-stats-daemon start

# 4. Take first snapshot
br-stats-history snapshot

# 5. Add to shell startup (optional)
echo 'alias stats="br-stats"' >> ~/.zshrc
```

### 🎯 What This Means

**Before:** Static numbers that could be questioned
**Now:** Live data pulled from actual git repos + GitHub API

**Interviewer says:** "These numbers seem high..."
**You respond:** *types `br-stats update`* "Here's the live data from my GitHub account right now."

**Result:** Instant credibility. They see it's real, current, and verifiable.

### 🔮 Coming Soon

- GitLab/Bitbucket integration
- Contribution graphs (ASCII art)
- Language breakdown by LOC
- Team collaboration metrics
- CI/CD pipeline stats
- Deployment frequency tracking

### ⚡ Pro Tips

1. **Run daemon on main machine** - keeps stats fresh
2. **Take daily snapshots** - build growth narrative
3. **Compare weekly** - show consistent velocity
4. **Share JSON exports** - verifiable data for applications
5. **Live demos** - run `br-stats update` during interviews

---

**The portfolio that updates itself. Because your work never stops.**
