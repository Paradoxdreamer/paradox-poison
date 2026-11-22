# Paradox Poison

LLMNR, NBT-NS, MDNS, and WPAD poisoner + credential harvester.

Classic internal network weapon for capturing NetNTLM hashes.

**Upstream:** [lgandx/Responder](https://github.com/lgandx/Responder)

---

## Install

### Linux

```bash
git clone https://github.com/lgandx/Responder.git
cd Responder
sudo python3 Responder.py -I eth0 -rdwv
```

### Termux

Works, but needs root or proper interface handling. Better on a real Linux box or Kali Nethunter.

```bash
pkg install python git
git clone https://github.com/lgandx/Responder.git
cd Responder
python Responder.py -h
```

---

## Typical Usage

```bash
sudo python3 Responder.py -I eth0 -rdwv
# then wait for hashes, or combine with ntlmrelayx
```

---

## Notes

- Extremely effective on Windows networks with LLMNR/NBT-NS enabled
- Modern environments may have mitigations (disable LLMNR, SMB signing, etc.)
- Always use on authorized networks only

Part of the Paradox internal kit.
