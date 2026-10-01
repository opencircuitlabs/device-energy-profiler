# Device Energy Profiler

`device-energy-profiler` turns voltage/current measurements and design budgets into repeatable electronics energy evidence for battery life, thermal design, efficiency targets, and lifecycle carbon models.

## Capabilities

- Trace chronology, field, and nonnegative-value validation
- Trapezoidal energy, charge, average, peak, and minimum power integration
- Operating-mode segmentation and measured duty cycles
- Synthetic duty-cycle daily/annual energy models
- Multi-rail output, conversion loss, limit, and source-margin budgets
- Converter efficiency curves and peak losses
- Capacity, usable fraction, aging, temperature, conversion, and quiescent battery runtime
- Junction temperature and thermal margin from conversion losses
- Baseline drift and within-trace spike detection
- Per-mode limit compliance and missing-measurement failures
- Before/after optimization comparisons
- Markdown measurement reports
- Dependency-free Node.js 18+ library and CLI

## Quick start

```bash
npm install
npm test
node src/cli.js validate examples/trace.json
node src/cli.js integrate examples/trace.json
node src/cli.js modes examples/trace.json examples/segments.json
```

## Library API

```js
import { integrateTrace, modeProfile, railBudget, batteryRuntime, annualEnergy } from '@opencircuitlabs/device-energy-profiler';
```

Measurement accuracy depends on instrument calibration, bandwidth, sampling, trigger coverage, wiring, and representative workloads. Battery and thermal estimates require product-specific validation and safety review.

## License

MIT. See [LICENSE](LICENSE).
