<template>
  <section>
    <!-- <div class="illustration-container">
      <v-image
        path="images/publications-illustration.svg"
        class="roadmap-illustration"
      />
    </div> -->
    <v-container>
      <v-stack direction="column">
        <app-section-descriptor title="Roadmap" heading="Neatio History & Roadmap" />
        <v-stack gap="1rem" class="laptop-remove">
          <v-dropdown
            v-model="selectedYear"
            :options="years"
            class="roadmap-dropdown"
          />
        </v-stack>
        <v-stack>
          <v-stack
            direction="column"
            style="margin: 1.5rem 6rem 0 0"
            class="tablet-remove mobile-remove"
          >
            <div v-for="year in years" :key="year">
              <v-chip
                class="clickable-chip"
                :class="{
                  'selected-year': selectedYear === year,
                }"
                @click="() => (selectedYear = year)"
              >
                <v-text :weight="600">{{ year }}</v-text>
              </v-chip>
            </div>
          </v-stack>
          <ul>
            <li
              v-for="item in roadmap[selectedYear]"
              :key="selectedYear + item.quarter"
            >
              <v-heading
                :level="4"
                :weight="600"
                font="serif"
                class="milestone-heading"
              >
                {{ item.quarter }} {{ selectedYear }}
              </v-heading>
              <div v-for="milestone in item.milestones" :key="milestone">
                <v-text
                  color="secondary"
                  :weight="400"
                  size="1.125rem"
                  class="milestone-description"
                >
                  {{ milestone }}
                </v-text>
              </div>
            </li>
          </ul>
        </v-stack>
      </v-stack>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'RoadmapList',
  data() {
    const selectedYear = new Date().getFullYear().toString()

    return {
      selectedYear,
      roadmap: {
        2021: [
        {
            quarter: 'Quarter 1',
            milestones: [
              'Neatio project development starts ✔️',
              ],
          },
          {
            quarter: 'Quarter 2',
            milestones: [
              'Neatio network testing - Closed Testnet ✔️',
            ],
          },
          {
            quarter: 'Quarter 3',
            milestones: [
              'Network stretching and bug fixes ✔️',
              ],
          },
          {
            quarter: 'Quarter 4',
            milestones: [
            'Neatio network testing - Public Testnet ✔️',
            ],
          },
        ],
        2022: [
        {
            quarter: 'Quarter 1',
            milestones: [
              'Neatio Mainnet launch ✔️',
              'Whitepaper 1.0 release ✔️',
              'The roadmap for 2022 revealed ✔️',
              'Neatio community build - Airdrop ✔️',
              ],
          },
          {
            quarter: 'Quarter 2',
            milestones: [
              'Neatio 2.0 web wallet development ✔️',
              'The new Neatio website development ✔️',
              'Whitepaper for Neatio 2.0 release ✔️',
              'NeatDocs documentation release ✔️',
              ],
          },
          {
            quarter: 'Quarter 3',
            milestones: [
              'New website 2.0 look redesign ✔️',
              'AMA sesion with HedgePay project ✔️',
              'Staking website gets a new look ✔️',
              'Neatio 2.0 explorer redesign ✔️',
              ],
          },
          {
            quarter: 'Quarter 4',
            milestones: [
              'Finexbox CEX listing of $NEAT ✔️',
              'Discord and telegram bots release ✔️',
              'AMA sesion with AnyDAO project ✔️',
              'December Quest Competition ✔️',
              ],
          },
        ],
        2023: [
        {
            quarter: 'Quarter 1',
            milestones: [
              '2023 Roadmap presentation ✔️',
              'Neatio Blog development & launch ✔️',
              'Bitcointalk bounty campaign start ✔️',
              'Governance development & implementation ✔️',
              ],
          },
          {
            quarter: 'Quarter 2',
            milestones: [
              '$NEAT token contracts development ✔️',
              'Crosschain bridge contracts development ✔️',              
              '$NEAT listing on DEX exchange ✔️',
              'Logo redesign for new $NIO network ✔️',
              'Whitepaper for Neatio 3.0 development ✔️',
              ],
          },
          {
            quarter: 'Quarter 3',
            milestones: [
              'Neatio network 3.0 development start ✔️',
              'The new website redesign and build ✔️',            
              'Contracts deployment on Polygon ✔️',
              'Uniswap v3 DEX $NIO token listing ✔️',
              'Undergoing native $NEAT coin swap ✔️'
              ],
          },
          {
            quarter: 'Quarter 4',
            milestones: [
              'Complete native $NEAT coin swap ✔️',
              'Neatio network 3.0 Testnet launch ✔️',
              'Neatio network 3.0 Mainnet launch ⏳',
              'New explorer for Neatio 3.0 development ⏳',
              'All-in-one wallet platform development ⏳',
              ],
          },
        ],
        // 2024: [
        // {
        //     quarter: 'Quarter 1',
        //     milestones: [
        //       'Neatio Milestone 1',
        //       'Neatio Milestone 2',
        //       'Neatio Milestone 3',
        //       ],
        //   },
        //   {
        //     quarter: 'Quarter 2',
        //     milestones: [
        //       'Neatio Milestone 1',
        //       'Neatio Milestone 2',
        //       'Neatio Milestone 3',
        //       ],
        //   },
        //   {
        //     quarter: 'Quarter 3',
        //     milestones: [
        //       'Neatio Milestone 1',
        //       'Neatio Milestone 2',
        //       'Neatio Milestone 3',
        //       ],
        //   },
        //   {
        //     quarter: 'Quarter 4',
        //     milestones: [
        //       'Neatio Milestone 1',
        //       'Neatio Milestone 2',
        //       'Neatio Milestone 3',
        //       ],
        //   },
        // ],
      },
    }
  },
  computed: {
    years() {
      return Object.keys(this.roadmap)
    },
  },
}
</script>

<style lang="postcss" scoped>
@import url('../lib/media-query-helper.css');

.roadmap-illustration {
  width: 100%;
  z-index: -1;
  margin-bottom: -12.5%;
}

.roadmap-dropdown {
  width: 50%;
  max-width: 12rem;
}

ul {
  padding: 0;
}

ul li {
  list-style: none;
}

.milestone-heading {
  margin: 1.5rem 0 0.5rem 0;
  font-size: 1.375rem;

  @media (--viewport-medium) {
    font-size: 1.25rem;
  }
}

.milestone-description {
  font-size: 1.375rem;
  line-height: 2rem;

  @media (--viewport-medium) {
    font-size: 1rem;
    line-height: 1.5rem;
  }
}

.clickable-chip {
  background: radial-gradient(
    134.5% 939.99% at -23.59% -12.9%,
    #262626 0%,
    rgba(26, 26, 26, 0.86293) 31.41%,
    rgba(32, 32, 32, 0.49) 100%
  );
  box-shadow: 4px 5px 4px rgba(0, 0, 0, 0.25);
  padding: 1.5rem 5rem;
  margin: 1rem 2rem 0.5rem 0;
  cursor: pointer;
}

.clickable-chip > * {
  font-size: 1.375rem;

  @media (--viewport-medium) {
    font-size: 1.25rem;
  }
}

.quarter {
  margin: 0.5rem 2rem 0.5rem 0;
  text-align: center;
  cursor: pointer;
}

.quarter > * {
  font-size: 1.25rem;
  line-height: 2.5rem;
}

.selected-year {
  border: 1px solid #5983fc;
  border-radius: 10px;
}

.selected-year > * {
  color:#5983fc;
  font-weight: 600;
}

.illustration-container {
  position: relative;
  z-index: -1;
}

.illustration-container::before {
  content: '';
  position: absolute;
  inset: -50% 0% -100% -50%;
  z-index: -1;
  background: radial-gradient(
    50% 50% at 50% 50%,
    rgba(248, 81, 142, 0.2) 0%,
    rgba(0, 0, 0, 0) 100%
  );
}
</style>
