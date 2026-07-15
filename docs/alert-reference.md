# Alert Reference

## LonghornVolumeDegraded

Severity: Warning

Meaning

One or more replicas are unavailable.

Possible causes

- Node reboot
- Replica rebuilding
- Network partition
- Disk failure

Recommended actions

- Check Longhorn UI
- Verify replica health
- Review longhorn-manager logs

---

## LonghornVolumeFaulted

Severity: Critical

Meaning

The volume has lost quorum and may no longer be accessible.

Immediate actions

- Identify failed replicas
- Restore redundancy
- Recover the volume
