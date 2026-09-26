# Tcp

VB6 Personal Alerter pair: the `PAlerter` client (`PAlerter.exe`) receives alerts over Winsock TCP, filters them by severity and group, announces them with Microsoft Agent and speech, logs to an Access database, and sits in the system tray; `AlerterMaster` is the server that tracks connected clients and sends alerts. `protocol.txt` documents the Distrotasks command protocol shared by both. Open `Client/Palerter.vbp` or `Master/AlerterMaster.vbp` in the VB6 IDE.

**Source last updated:** 2001-03-26 · **Language:** VB6 · **Target:** VB6 Win32 · **Output:** WinForms exe

## Solution structure

| Project | Language | Type | Purpose |
|---------|----------|------|---------|
| `PAlerter` (`Client/Palerter.vbp`) | VB6 | WinForms exe | Personal Alerter TCP client with Agent speech, filters, and tray icon |
| `AlerterMaster` (`Master/AlerterMaster.vbp`) | VB6 | WinForms exe | Alerter master server that sends alerts to connected clients |

## How to open

Open the `.vbp` in Visual Basic 6.0 IDE:
- `Client/Palerter.vbp`
- `Master/AlerterMaster.vbp`

## Requirements

- Visual Basic 6.0 IDE
- Microsoft ActiveX Data Objects 2.5 / 2.6
- Microsoft Winsock control (MSWINSCK.OCX)
- Client only: Microsoft Agent 2.0, VoiceText 1.0, TABCTL32.OCX, COMDLG32.OCX, systray.ocx

## Attribution and provenance

Working copy from my Historical Dev folder `VB/Old/Tcp` (GitHub repo Tcp-VB6). Both projects note "Includes Logging & TCPIP Server" in their version comments.

## License

MIT © 2026 VaderConsulting for Dave Robinson's code. See `LICENSE`.
