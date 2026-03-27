<!-- description: Immunity.reg: massive HKCU P3P History dword entries for ad/tracking hosts—IE-era cookie/P3P policy; merge only if you understand impact. -->

# Immunity

**`Immunity.reg`** is a **Windows Registry** file that adds a very large set of keys under:

**`HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Internet Settings\P3P\History\`**

Each subkey is a **hostname** (or IP) with a **`DWORD`** value (often **`5`** in the header lines). This aligns with legacy **Internet Explorer / WinINET P3P “cookie policy”** storage—effectively pre-seeding **per-site** P3P history entries for many **ad / tracking**-related domains.

**Notes**

- Modern browsers may **ignore** much of this for their own cookie logic; impact is mostly relevant to **WinINET**-based stacks and compatibility scenarios.
- The file is **huge** (hundreds of thousands of lines)—**diff/review** in chunks before merging.
- **Backup** **`HKCU`** or create a **restore point** before **`reg import`**.

---

## Usage

```cmd
reg import Immunity.reg
```

Prefer testing on a **non-production** user profile first.

---

## Disclaimer

**NO WARRANTY.** THERE IS NO WARRANTY FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW. EXCEPT WHEN OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU. SHOULD THE PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING, REPAIR OR CORRECTION.

**Limitation of Liability.** IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MODIFIES AND/OR CONVEYS THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES, INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

---

## Explained like you're five (the honest kind)

Your PC is a **busy kitchen**. This repo is at best a **sticky note on the fridge**: it might remind you where the knives are, but it does not make you a Michelin chef, and it definitely does not stop someone from sneaking in through the window. We use simple words on purpose so nobody confuses scripts with superpowers.

---

## Disclaimer (read this; it matters)

This software and documentation are provided **“as is”**, without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. **Use at your own risk.**

If you do not agree, **do not use** this repository.
